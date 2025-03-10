<template>
    <div class="min-h-screen dark:bg-gray-900">
      <!-- Hero区域 -->
      <div class="relative h-screen">
        <div class="absolute inset-0">
          <img src="https://ai-public.mastergo.com/ai/img_res/48a01c9382ba161b28ae3c4fcb1ea5d0.jpg"
               class="w-full h-full object-cover" 
               alt="背景">
        </div>
        
        <div class="relative container mx-auto px-4 h-full flex items-center">
          <div class="max-w-2xl text-white">
            <h1 class="text-6xl font-bold mb-6 ml-20">臻选好茶，品味人生</h1>
            <p class="text-xl mb-8">源自千年茶道精髓，传承东方茶文化瑰宝</p>
            <button class="bg-green-600 text-white px-8 py-3 text-lg !rounded-button hover:bg-green-700 transition-colors whitespace-nowrap">
              了解更多
            </button>
          </div>
        </div>
      </div>
  
      <!-- 产品系列 -->
      <section class="py-20 bg-green-50 dark:bg-gray-800">
        <div class="container mx-auto px-4">
          <h2 class="text-3xl font-bold text-center mb-12 dark:text-white">精选茶系列</h2>
          <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div v-for="(item, index) in products" 
                 :key="index" 
                 class="bg-white dark:bg-gray-700 rounded-lg overflow-hidden shadow-md hover:shadow-lg transition-shadow">
              <div class="h-64 overflow-hidden">
                <img :src="item.image" 
                     :alt="item.name"
                     class="w-full h-full object-cover">
              </div>
              <div class="p-6">
                <h3 class="text-xl font-bold mb-2 dark:text-white">{{ item.name }}</h3>
                <p class="text-gray-600 dark:text-gray-300 mb-4">{{ item.desc }}</p>
                <button class="text-green-600 dark:text-green-400 font-medium !rounded-button hover:text-green-700 dark:hover:text-green-300 whitespace-nowrap">
                  查看详情
                  <i class="fas fa-arrow-right ml-2"></i>
                </button>
              </div>
            </div>
          </div>
        </div>
      </section>
  
      <!-- 品牌故事 -->
      <section class="py-20 dark:bg-gray-900">
        <div class="container mx-auto px-4">
          <div class="flex flex-col md:flex-row items-center gap-12">
            <div class="w-full md:w-1/2">
              <img src="https://ai-public.mastergo.com/ai/img_res/018575f28167cbdfc02cce2c2b63ec4d.jpg"
                   alt="品牌故事"
                   class="rounded-lg shadow-lg w-full">
            </div>
            <div class="w-full md:w-1/2">
              <h2 class="text-3xl font-bold mb-6 dark:text-white">匠心传承，品质如一</h2>
              <p class="text-gray-600 dark:text-gray-300 mb-4 leading-relaxed">
                我们秉承着对茶文化的热爱与追求，精心挑选来自世界各地的优质茶叶。从茶园到茶杯，每一个环节都严格把控，只为给您最纯粹的茶香体验。
              </p>
              <p class="text-gray-600 dark:text-gray-300 mb-6 leading-relaxed">
                二十载匠心经营，服务超过千万茶友。让更多人感受东方茶道之美，是我们不变的初心。
              </p>
              <button class="bg-green-600 text-white px-6 py-3 !rounded-button hover:bg-green-700 transition-colors whitespace-nowrap">
                了解品牌故事
              </button>
            </div>
          </div>
        </div>
      </section>
    </div>
  </template>
  
  <script>
  export default {
    name: 'App',
    data() {
      return {
        products: [
          {
            name: '明前龙井',
            desc: '采自西湖龙井核心产区，清香持久，回甘悠长',
            image: 'https://ai-public.mastergo.com/ai/img_res/f6c56b5b436faf810816399d0ed6962a.jpg'
          },
          {
            name: '大红袍',
            desc: '武夷山原产，岩骨花香，醇厚耐泡',
            image: 'https://ai-public.mastergo.com/ai/img_res/97f84c81e7e3139874bbc0850ebff68b.jpg'
          },
          {
            name: '白毫银针',
            desc: '福鼎特级白茶，一芽一叶，滋味甘醇',
            image: 'https://ai-public.mastergo.com/ai/img_res/efc9edc6edaf3826318cb0edb16ae60e.jpg'
          }
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  .nav-link {
    color: #374151;
    font-weight: 500;
    transition: color 0.2s;
  }
  
  .nav-link:hover {
    color: #047857;
  }
  
  .lang-btn {
    padding: 0.5rem 1rem;
    background-color: #f3f4f6;
    color: #374151;
    font-weight: 500;
    transition: all 0.2s;
  }
  
  .lang-btn:hover {
    background-color: #e5e7eb;
  }
  
  .contact-btn {
    padding: 0.5rem 1rem;
    background-color: #047857;
    color: white;
    font-weight: 500;
    transition: all 0.2s;
  }
  
  .contact-btn:hover {
    background-color: #065f46;
  }
  </style>
  
  