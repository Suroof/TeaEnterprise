<template>
  <div class="about min-h-screen pt-16">
    <!-- 品牌介绍头部 -->
    <div class="bg-green-600 text-white py-12">
      <div class="container mx-auto px-4">
        <h1 class="text-4xl font-bold text-center mb-6">关于臻茗</h1>
        <p class="text-center text-lg max-w-3xl mx-auto">臻茗茶业成立于2010年，是一家专注于传统茶文化传承与创新的企业，致力于将中国优质茶文化带给全世界的茶爱好者</p>
      </div>
    </div>
    
    <!-- 品牌故事 -->
    <div class="container mx-auto px-4 py-16">
      <div class="flex flex-col md:flex-row items-center gap-12 mb-20">
        <div class="w-full md:w-1/2">
          <img src="https://ai-public.mastergo.com/ai/img_res/018575f28167cbdfc02cce2c2b63ec4d.jpg" 
               alt="品牌故事" 
               class="rounded-lg shadow-xl w-full">
        </div>
        <div class="w-full md:w-1/2">
          <h2 class="text-3xl font-bold mb-6 text-gray-800">品牌故事</h2>
          <div class="space-y-4 text-gray-600">
            <p class="leading-relaxed">臻茗茶业的创始人王明远先生出生于福建安溪的一个茶农家庭，从小耳濡目染茶文化的精髓。大学毕业后，他放弃了城市的高薪工作，回到家乡，决心将家族几代人的制茶技艺发扬光大。</p>
            <p class="leading-relaxed">2010年，王明远先生创立了臻茗茶业，以"臻品好茶，茗享生活"为理念，致力于寻找中国各地的优质茶叶，并将其带给热爱茶文化的人们。</p>
            <p class="leading-relaxed">十余年来，臻茗茶业从最初的一家小店发展成为拥有全国200多家连锁门店的知名茶企，产品远销海外30多个国家和地区，成为中国茶文化的重要传播者。</p>
          </div>
        </div>
      </div>
      
      <!-- 企业使命与愿景 -->
      <div class="bg-green-50 rounded-xl p-8 md:p-12 mb-20">
        <div class="text-center mb-12">
          <h2 class="text-3xl font-bold mb-4 text-gray-800">企业使命与愿景</h2>
          <p class="text-gray-600 max-w-3xl mx-auto">我们致力于传承和创新中国茶文化，让更多人体验茶的魅力</p>
        </div>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div class="bg-white p-6 rounded-lg shadow-md text-center">
            <div class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <i class="fas fa-leaf text-green-600 text-2xl"></i>
            </div>
            <h3 class="text-xl font-bold mb-3 text-gray-800">使命</h3>
            <p class="text-gray-600">传承中国茶文化，推广健康生活方式，让更多人了解茶的文化与价值。</p>
          </div>
          
          <div class="bg-white p-6 rounded-lg shadow-md text-center">
            <div class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <i class="fas fa-eye text-green-600 text-2xl"></i>
            </div>
            <h3 class="text-xl font-bold mb-3 text-gray-800">愿景</h3>
            <p class="text-gray-600">成为全球领先的茶文化传播者，让臻茗茶成为品质与文化的代名词。</p>
          </div>
          
          <div class="bg-white p-6 rounded-lg shadow-md text-center">
            <div class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <i class="fas fa-heart text-green-600 text-2xl"></i>
            </div>
            <h3 class="text-xl font-bold mb-3 text-gray-800">价值观</h3>
            <p class="text-gray-600">品质至上，文化传承，创新发展，共享共赢。</p>
          </div>
        </div>
      </div>
      
      <!-- 发展历程 -->
      <div class="mb-20">
        <h2 class="text-3xl font-bold mb-8 text-center text-gray-800">发展历程</h2>
        <div class="relative">
          <!-- 时间轴 -->
          <div class="hidden md:block absolute left-1/2 transform -translate-x-1/2 h-full w-1 bg-green-200"></div>
          
          <!-- 时间点 -->
          <div class="space-y-12">
            <div class="flex flex-col md:flex-row items-center">
              <div class="md:w-1/2 md:pr-12 md:text-right">
                <h3 class="text-xl font-bold text-green-600">2010年</h3>
                <p class="text-gray-600 mt-2">臻茗茶业在福建安溪成立，开设第一家门店</p>
              </div>
              <div class="md:w-1/2 md:pl-12 mt-4 md:mt-0">
                <div class="w-8 h-8 bg-green-500 rounded-full mx-auto md:mx-0 md:-ml-4 relative z-10 flex items-center justify-center">
                  <i class="fas fa-star text-white text-xs"></i>
                </div>
              </div>
            </div>
            
            <div class="flex flex-col md:flex-row-reverse items-center">
              <div class="md:w-1/2 md:pl-12">
                <h3 class="text-xl font-bold text-green-600">2015年</h3>
                <p class="text-gray-600 mt-2">全国门店数量突破50家，开始进军国际市场</p>
              </div>
              <div class="md:w-1/2 md:pr-12 mt-4 md:mt-0">
                <div class="w-8 h-8 bg-green-500 rounded-full mx-auto md:mx-0 md:ml-auto md:-mr-4 relative z-10 flex items-center justify-center">
                  <i class="fas fa-globe text-white text-xs"></i>
                </div>
              </div>
            </div>
            
            <div class="flex flex-col md:flex-row items-center">
              <div class="md:w-1/2 md:pr-12 md:text-right">
                <h3 class="text-xl font-bold text-green-600">2020年</h3>
                <p class="text-gray-600 mt-2">成立臻茗茶文化研究院，深入研究茶文化传承与创新</p>
              </div>
              <div class="md:w-1/2 md:pl-12 mt-4 md:mt-0">
                <div class="w-8 h-8 bg-green-500 rounded-full mx-auto md:mx-0 md:-ml-4 relative z-10 flex items-center justify-center">
                  <i class="fas fa-book text-white text-xs"></i>
                </div>
              </div>
            </div>
            
            <div class="flex flex-col md:flex-row-reverse items-center">
              <div class="md:w-1/2 md:pl-12">
                <h3 class="text-xl font-bold text-green-600">2023年</h3>
                <p class="text-gray-600 mt-2">全国门店突破200家，产品远销30多个国家和地区</p>
              </div>
              <div class="md:w-1/2 md:pr-12 mt-4 md:mt-0">
                <div class="w-8 h-8 bg-green-500 rounded-full mx-auto md:mx-0 md:ml-auto md:-mr-4 relative z-10 flex items-center justify-center">
                  <i class="fas fa-award text-white text-xs"></i>
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
  name: 'AboutView'
}
</script>
