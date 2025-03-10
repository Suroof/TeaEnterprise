<template>
  <div class="stores min-h-screen pt-16">
    <!-- 门店搜索区域 -->
    <div class="bg-green-600 text-white py-12">
      <div class="container mx-auto px-4">
        <h1 class="text-4xl font-bold text-center mb-6">门店查询</h1>
        <p class="text-center text-lg mb-8">全国超过200家门店，找到离您最近的臻茗茶业</p>
        
        <div class="max-w-2xl mx-auto flex flex-col md:flex-row gap-4">
          <div class="flex-grow">
            <div class="relative">
              <i class="fas fa-search absolute left-4 top-1/2 transform -translate-y-1/2 text-gray-400"></i>
              <input 
                type="text" 
                placeholder="输入城市、区域或门店名称" 
                class="w-full pl-12 pr-4 py-3 rounded-lg text-gray-800 focus:outline-none focus:ring-2 focus:ring-green-800"
                v-model="searchQuery"
              >
            </div>
          </div>
          <button 
            class="bg-green-800 hover:bg-green-900 text-white px-6 py-3 rounded-lg transition duration-300 whitespace-nowrap"
            @click="searchStores"
          >
            <i class="fas fa-search mr-2"></i>查找门店
          </button>
        </div>
      </div>
    </div>
    
    <!-- 地图与门店列表区域 -->
    <div class="container mx-auto px-4 py-12">
      <div class="flex flex-col lg:flex-row gap-8">
        <!-- 地图区域 -->
        <div class="w-full lg:w-2/3 bg-gray-100 rounded-lg overflow-hidden shadow-lg" style="height: 500px;">
          <div class="h-full w-full">
            <!-- 使用百度地图静态图API -->
            <img 
              src="../../public/image/map.jpg" 
              alt="茶店地图" 
              class="w-full h-full object-cover"
            >
          </div>
        </div>
        
        <!-- 门店列表 -->
        <div class="w-full lg:w-1/3">
          <div class="bg-white rounded-lg shadow-lg p-6 mb-6">
            <h2 class="text-xl font-bold mb-4 flex items-center">
              <i class="fas fa-filter mr-2 text-green-600"></i>筛选
            </h2>
            <div class="space-y-4">
              <div>
                <label class="block text-gray-700 mb-2">选择城市</label>
                <select class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-green-500" v-model="selectedCity">
                  <option value="">全部城市</option>
                  <option v-for="(city, index) in cities" :key="index" :value="city">{{ city }}</option>
                </select>
              </div>
              <div>
                <label class="block text-gray-700 mb-2">门店类型</label>
                <div class="flex flex-wrap gap-2">
                  <button 
                    v-for="(type, index) in storeTypes" 
                    :key="index"
                    @click="toggleStoreType(type.id)"
                    :class="[`px-3 py-1 rounded-full border transition-colors text-sm`, 
                            selectedTypes.includes(type.id) ? 'bg-green-600 text-white border-green-600' : 'border-gray-300 text-gray-700']"
                  >
                    {{ type.name }}
                  </button>
                </div>
              </div>
            </div>
          </div>
          
          <div class="bg-white rounded-lg shadow-lg overflow-hidden">
            <h2 class="text-xl font-bold p-6 border-b">
              <span class="text-green-600">{{ filteredStores.length }}</span> 家门店
            </h2>
            <div class="divide-y max-h-[400px] overflow-y-auto">
              <div 
                v-for="(store, index) in filteredStores" 
                :key="index"
                class="p-4 hover:bg-green-50 transition-colors cursor-pointer"
                @click="selectStore(store)"
              >
                <h3 class="font-bold text-lg mb-1">{{ store.name }}</h3>
                <p class="text-gray-600 text-sm mb-2">{{ store.address }}</p>
                <div class="flex justify-between items-center">
                  <span class="text-xs px-2 py-1 bg-green-100 text-green-800 rounded-full">{{ store.type }}</span>
                  <button class="text-green-600 text-sm flex items-center">
                    <i class="fas fa-directions mr-1"></i> 查看路线
                  </button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'StoresPage',
  data() {
    return {
      searchQuery: '',
      selectedCity: '',
      selectedTypes: ['flagship', 'standard'],
      cities: ['北京', '上海', '广州', '深圳', '杭州', '成都', '武汉', '南京'],
      storeTypes: [
        { id: 'flagship', name: '旗舰店' },
        { id: 'standard', name: '标准店' },
        { id: 'express', name: '快闪店' },
        { id: 'experience', name: '体验店' }
      ],
      stores: [
        {
          id: 1,
          name: '臻茗茶业北京三里屯旗舰店',
          address: '北京市朝阳区三里屯太古里北区N8-30',
          city: '北京',
          type: '旗舰店',
          typeId: 'flagship',
          phone: '010-64516789',
          hours: '10:00-22:00',
          lat: 39.938227,
          lng: 116.455847
        },
        {
          id: 2,
          name: '臻茗茶业上海南京东路店',
          address: '上海市黄浦区南京东路299号',
          city: '上海',
          type: '标准店',
          typeId: 'standard',
          phone: '021-63280888',
          hours: '09:30-21:30',
          lat: 31.236230,
          lng: 121.480539
        },
        {
          id: 3,
          name: '臻茗茶业广州天河城店',
          address: '广州市天河区天河路208号天河城百货4楼',
          city: '广州',
          type: '标准店',
          typeId: 'standard',
          phone: '020-85337868',
          hours: '10:00-22:00',
          lat: 23.132631,
          lng: 113.327850
        },
        {
          id: 4,
          name: '臻茗茶业深圳万象城店',
          address: '深圳市罗湖区宝安南路1881号万象城L2层',
          city: '深圳',
          type: '旗舰店',
          typeId: 'flagship',
          phone: '0755-82668899',
          hours: '10:00-22:00',
          lat: 22.544700,
          lng: 114.109497
        },
        {
          id: 5,
          name: '臻茗茶业杭州西湖体验店',
          address: '杭州市西湖区南山路98号',
          city: '杭州',
          type: '体验店',
          typeId: 'experience',
          phone: '0571-87965432',
          hours: '09:00-18:00',
          lat: 30.242414,
          lng: 120.148722
        },
        {
          id: 6,
          name: '臻茗茶业成都春熙路店',
          address: '成都市锦江区春熙路299号',
          city: '成都',
          type: '标准店',
          typeId: 'standard',
          phone: '028-86698765',
          hours: '10:00-22:00',
          lat: 30.659828,
          lng: 104.081534
        },
        {
          id: 7,
          name: '臻茗茶业武汉光谷快闪店',
          address: '武汉市洪山区光谷广场步行街B区',
          city: '武汉',
          type: '快闪店',
          typeId: 'express',
          phone: '027-87654321',
          hours: '10:00-21:00',
          lat: 30.507462,
          lng: 114.419876
        }
      ]
    }
  },
  computed: {
    filteredStores() {
      return this.stores.filter(store => {
        // 城市筛选
        if (this.selectedCity && store.city !== this.selectedCity) {
          return false;
        }
        
        // 类型筛选
        if (this.selectedTypes.length > 0 && !this.selectedTypes.includes(store.typeId)) {
          return false;
        }
        
        // 搜索筛选
        if (this.searchQuery) {
          const query = this.searchQuery.toLowerCase();
          return store.name.toLowerCase().includes(query) || 
                 store.address.toLowerCase().includes(query) || 
                 store.city.toLowerCase().includes(query);
        }
        
        return true;
      });
    }
  },
  methods: {
    toggleStoreType(typeId) {
      const index = this.selectedTypes.indexOf(typeId);
      if (index > -1) {
        this.selectedTypes.splice(index, 1);
      } else {
        this.selectedTypes.push(typeId);
      }
    },
    searchStores() {
      // 实际项目中可能需要调用API进行搜索
      console.log('搜索门店:', this.searchQuery);
    },
    selectStore(store) {
      console.log('选择门店:', store);
      // 实际项目中可能需要在地图上显示该门店位置
    }
  }
}
</script>