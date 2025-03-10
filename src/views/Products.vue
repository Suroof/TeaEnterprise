<template>
  <div class="products min-h-screen pt-16">
    <!-- 产品分类导航 -->
    <div class="bg-green-600 text-white py-4">
      <div class="container mx-auto px-4">
        <div class="flex flex-wrap justify-center space-x-2 md:space-x-8">
          <button 
            v-for="(category, index) in categories" 
            :key="index"
            @click="activeCategory = category.id"
            :class="[`px-4 py-2 rounded-full transition-colors`, 
                    activeCategory === category.id ? 'bg-white text-green-600 font-bold' : 'hover:bg-green-700']"
          >
            {{ category.name }}
          </button>
        </div>
      </div>
    </div>
    
    <div class="container mx-auto px-4 py-12">
      <h1 class="text-4xl font-bold text-center mb-2">精选茶品</h1>
      <p class="text-gray-600 text-center mb-12">甄选世界各地优质茶叶，传承千年茶道精髓</p>
      
      <!-- 产品筛选 -->
      <div class="mb-8 flex flex-wrap justify-center gap-4">
        <button 
          class="px-4 py-2 rounded-lg border border-gray-300 hover:border-green-600 hover:text-green-600 transition-colors"
          :class="{'border-green-600 text-green-600': sortBy === 'popular'}"
          @click="sortBy = 'popular'"
        >
          <i class="fas fa-fire mr-2"></i>热门推荐
        </button>
        <button 
          class="px-4 py-2 rounded-lg border border-gray-300 hover:border-green-600 hover:text-green-600 transition-colors"
          :class="{'border-green-600 text-green-600': sortBy === 'new'}"
          @click="sortBy = 'new'"
        >
          <i class="fas fa-star mr-2"></i>新品上市
        </button>
        <button 
          class="px-4 py-2 rounded-lg border border-gray-300 hover:border-green-600 hover:text-green-600 transition-colors"
          :class="{'border-green-600 text-green-600': sortBy === 'price'}"
          @click="sortBy = 'price'"
        >
          <i class="fas fa-sort-amount-down mr-2"></i>价格排序
        </button>
      </div>
      
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- 产品卡片 1 -->
        <div class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-xl transition-shadow duration-300">
          <div class="h-64 overflow-hidden relative group">
            <img src="https://ai-public.mastergo.com/ai/img_res/f6c56b5b436faf810816399d0ed6962a.jpg" 
                 alt="龙井茶" 
                 class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
            <div class="absolute top-2 right-2 bg-green-600 text-white text-xs font-bold px-2 py-1 rounded-full">明前特级</div>
          </div>
          <div class="p-6">
            <div class="flex justify-between items-start mb-2">
              <h2 class="text-xl font-semibold">西湖龙井</h2>
              <div class="flex items-center">
                <i class="fas fa-star text-yellow-400"></i>
                <span class="ml-1 text-sm text-gray-600">4.9</span>
              </div>
            </div>
            <p class="text-gray-600 mb-4">产自杭州西湖龙井村，清香味，形状扁平挺直，色泽嫩绿光润，口感鲜爽回甘。</p>
            <div class="flex justify-between items-center">
              <div>
                <span class="text-green-700 font-bold text-xl">¥128.00</span>
                <span class="text-gray-400 text-sm line-through ml-2">¥168.00</span>
              </div>
              <button class="bg-green-600 hover:bg-green-700 text-white px-4 py-2 rounded-lg transition duration-300 flex items-center">
                <i class="fas fa-shopping-cart mr-2"></i>加入购物车
              </button>
            </div>
          </div>
        </div>
        
        <!-- 产品卡片 2 -->
        <div class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-xl transition-shadow duration-300">
          <div class="h-64 overflow-hidden relative group">
            <img src="https://ai-public.mastergo.com/ai/img_res/97f84c81e7e3139874bbc0850ebff68b.jpg" 
                 alt="铁观音" 
                 class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
            <div class="absolute top-2 right-2 bg-red-600 text-white text-xs font-bold px-2 py-1 rounded-full">限时特惠</div>
          </div>
          <div class="p-6">
            <div class="flex justify-between items-start mb-2">
              <h2 class="text-xl font-semibold">安溪铁观音</h2>
              <div class="flex items-center">
                <i class="fas fa-star text-yellow-400"></i>
                <span class="ml-1 text-sm text-gray-600">4.8</span>
              </div>
            </div>
            <p class="text-gray-600 mb-4">产自福建安溪，香气馥郁持久，滋味醇厚甘鲜，回甘明显，韵味悠长。</p>
            <div class="flex justify-between items-center">
              <div>
                <span class="text-green-700 font-bold text-xl">¥168.00</span>
                <span class="text-gray-400 text-sm line-through ml-2">¥198.00</span>
              </div>
              <button class="bg-green-600 hover:bg-green-700 text-white px-4 py-2 rounded-lg transition duration-300 flex items-center">
                <i class="fas fa-shopping-cart mr-2"></i>加入购物车
              </button>
            </div>
          </div>
        </div>
        
        <!-- 产品卡片 3 -->
        <div class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-xl transition-shadow duration-300">
          <div class="h-64 overflow-hidden relative group">
            <img src="https://ai-public.mastergo.com/ai/img_res/efc9edc6edaf3826318cb0edb16ae60e.jpg" 
                 alt="普洱茶" 
                 class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
            <div class="absolute top-2 right-2 bg-purple-600 text-white text-xs font-bold px-2 py-1 rounded-full">陈年珍藏</div>
          </div>
          <div class="p-6">
            <div class="flex justify-between items-start mb-2">
              <h2 class="text-xl font-semibold">云南普洱</h2>
              <div class="flex items-center">
                <i class="fas fa-star text-yellow-400"></i>
                <span class="ml-1 text-sm text-gray-600">4.7</span>
              </div>
            </div>
            <p class="text-gray-600 mb-4">产自云南，经过特殊工艺发酵，具有独特陈香，越陈越香，有助消化解腻。</p>
            <div class="flex justify-between items-center">
              <div>
                <span class="text-green-700 font-bold text-xl">¥198.00</span>
                <span class="text-gray-400 text-sm line-through ml-2">¥258.00</span>
              </div>
              <button class="bg-green-600 hover:bg-green-700 text-white px-4 py-2 rounded-lg transition duration-300 flex items-center">
                <i class="fas fa-shopping-cart mr-2"></i>加入购物车
              </button>
            </div>
          </div>
        </div>
        
        <!-- 产品卡片 4 -->
        <div class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-xl transition-shadow duration-300">
          <div class="h-64 overflow-hidden relative group">
            <img src="https://ai-public.mastergo.com/ai/img_res/97f84c81e7e3139874bbc0850ebff68b.jpg" 
                 alt="大红袍" 
                 class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
            <div class="absolute top-2 right-2 bg-yellow-600 text-white text-xs font-bold px-2 py-1 rounded-full">稀有品种</div>
          </div>
          <div class="p-6">
            <div class="flex justify-between items-start mb-2">
              <h2 class="text-xl font-semibold">武夷大红袍</h2>
              <div class="flex items-center">
                <i class="fas fa-star text-yellow-400"></i>
                <span class="ml-1 text-sm text-gray-600">4.9</span>
              </div>
            </div>
            <p class="text-gray-600 mb-4">产自武夷山，岩韵明显，香气高锐持久，滋味浓烈。</p>
            <div class="flex justify-between items-center">
              <div>
                <span class="text-green-700 font-bold text-xl">¥258.00</span>
                <span class="text-gray-400 text-sm line-through ml-2">¥328.00</span>
              </div>
              <button class="bg-green-600 hover:bg-green-700 text-white px-4 py-2 rounded-lg transition duration-300 flex items-center">
                <i class="fas fa-shopping-cart mr-2"></i>加入购物车
              </button>
            </div>
          </div>
        </div>
        
        <!-- 产品卡片 5 -->
        <div class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-xl transition-shadow duration-300">
          <div class="h-64 overflow-hidden relative group">
            <img src="https://ai-public.mastergo.com/ai/img_res/f6c56b5b436faf810816399d0ed6962a.jpg" 
                 alt="碧螺春" 
                 class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
            <div class="absolute top-2 right-2 bg-blue-600 text-white text-xs font-bold px-2 py-1 rounded-full">口粮首选</div>
          </div>
          <div class="p-6">
            <div class="flex justify-between items-start mb-2">
              <h2 class="text-xl font-semibold">洞庭碧螺春</h2>
              <div class="flex items-center">
                <i class="fas fa-star text-yellow-400"></i>
                <span class="ml-1 text-sm text-gray-600">4.6</span>
              </div>
            </div>
            <p class="text-gray-600 mb-4">产自江苏太湖洞庭山，形似螺，香气清新，滋味鲜爽，汤色清澈明亮。</p>
            <div class="flex justify-between items-center">
              <div>
                <span class="text-green-700 font-bold text-xl">¥148.00</span>
                <span class="text-gray-400 text-sm line-through ml-2">¥188.00</span>
              </div>
              <button class="bg-green-600 hover:bg-green-700 text-white px-4 py-2 rounded-lg transition duration-300 flex items-center">
                <i class="fas fa-shopping-cart mr-2"></i>加入购物车
              </button>
            </div>
          </div>
        </div>
        
        <!-- 产品卡片 6 -->
        <div class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-xl transition-shadow duration-300">
          <div class="h-64 overflow-hidden relative group">
            <img src="https://ai-public.mastergo.com/ai/img_res/efc9edc6edaf3826318cb0edb16ae60e.jpg" 
                 alt="金骏眉" 
                 class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500">
            <div class="absolute top-2 right-2 bg-orange-600 text-white text-xs font-bold px-2 py-1 rounded-full">新品上市</div>
          </div>
          <div class="p-6">
            <div class="flex justify-between items-start mb-2">
              <h2 class="text-xl font-semibold">正山小种金骏眉</h2>
              <div class="flex items-center">
                <i class="fas fa-star text-yellow-400"></i>
                <span class="ml-1 text-sm text-gray-600">4.8</span>
              </div>
            </div>
            <p class="text-gray-600 mb-4">产自福建武夷山，外形细小紧密，色泽乌黑油润，香气馥郁，滋味醇厚。</p>
            <div class="flex justify-between items-center">
              <div>
                <span class="text-green-700 font-bold text-xl">¥188.00</span>
                <span class="text-gray-400 text-sm line-through ml-2">¥228.00</span>
              </div>
              <button class="bg-green-600 hover:bg-green-700 text-white px-4 py-2 rounded-lg transition duration-300 flex items-center">
                <i class="fas fa-shopping-cart mr-2"></i>加入购物车
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductsPage',
  data() {
    return {
      activeCategory: 'all',
      sortBy: 'popular',
      categories: [
        { id: 'all', name: '全部茶品' },
        { id: 'green', name: '绿茶' },
        { id: 'black', name: '红茶' },
        { id: 'oolong', name: '乌龙茶' },
        { id: 'white', name: '白茶' },
        { id: 'puer', name: '普洱茶' },
        { id: 'herbal', name: '花草茶' }
      ]
    }
  }
}
</script>