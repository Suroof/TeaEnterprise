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
            <p class="text-gray-600">传承中国茶文化，推广健康生活方式，让更多人了解茶的魅力与价值。</p>
          </div>
          
          <div class="bg-white p-6 rounded-lg shadow-md text-center">
            <div class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <i class="fas fa-eye text-green-600 text-2xl"></i>
            </div>
            <h3 class="text-xl font-bold mb-3 text-gray-800">愿景</h3>
            <p class="text-gray-600">成为全球最受尊敬的中国茶文化传播者，让中国茶香飘向世界每一个角落。</p>
          </div>
          
          <div class="bg-white p-6 rounded-lg shadow-md text-center">
            <div class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mx-auto mb-4">
              <i class="fas fa-heart text-green-600 text-2xl"></i>
            </div>
            <h3 class="text-xl font-bold mb-3 text-gray-800">价值观</h3>
            <p class="text-gray-600">诚信、品质、创新、共赢，以客户满意为中心，以品质为生命，以创新为动力。</p>
          </div>
        </div>
      </div>
      
      <!-- 发展历程 -->
      <div class="mb-20">
        <h2 class="text-3xl font-bold mb-12 text-center text-gray-800">发展历程</h2>
        
        <div class="relative">
          <!-- 时间轴线 -->
          <div class="absolute left-1/2 transform -translate-x-1/2 h-full w-1 bg-green-200"></div>
          
          <!-- 时间节点 -->
          <div class="space-y-24 relative">
            <!-- 2010年 -->
            <div class="flex flex-col md:flex-row items-center">
              <div class="md:w-1/2 md:pr-12 md:text-right mb-4 md:mb-0">
                <h3 class="text-2xl font-bold text-green-600">2010年</h3>
                <p class="text-gray-600 mt-2">臻茗茶业在福建安溪成立，开设第一家实体店</p>
              </div>
              <div class="md:w-1/2 md:pl-12 flex justify-start">
                <div class="w-12 h-12 rounded-full bg-green-600 border-4 border-green-100 flex items-center justify-center z-10">
                  <i class="fas fa-store text-white"></i>
                </div>
              </div>
            </div>
            
            <!-- 2013年 -->
            <div class="flex flex-col md:flex-row items-center">
              <div class="md:w-1/2 md:pr-12 flex justify-end order-1 md:order-1">
                <div class="w-12 h-12 rounded-full bg-green-600 border-4 border-green-100 flex items-center justify-center z-10">
                  <i class="fas fa-award text-white"></i>
                </div>
              </div>
              <div class="md:w-1/2 md:pl-12 md:text-left mb-4 md:mb-0 order-2 md:order-2">
                <h3 class="text-2xl font-bold text-green-600">2013年</h3>
                <p class="text-gray-600 mt-2">获得"中国茶叶行业新锐品牌"称号，开始在全国范围内拓展连锁店</p>
              </div>
            </div>
            
            <!-- 2016年 -->
            <div class="flex flex-col md:flex-row items-center">
              <div class="md:w-1/2 md:pr-12 md:text-right mb-4 md:mb-0">
                <h3 class="text-2xl font-bold text-green-600">2016年</h3>
                <p class="text-gray-600 mt-2">成立臻茗茶文化研究院，开始系统性研究和传播中国茶文化</p>
              </div>
              <div class="md:w-1/2 md:pl-12 flex justify-start">
                <div class="w-12 h-12 rounded-full bg-green-600 border-4 border-green-100 flex items-center justify-center z-10">
                  <i class="fas fa-book text-white"></i>
                </div>
              </div>
            </div>
            
            <!-- 2020年 -->
            <div class="flex flex-col md:flex-row items-center">
              <div class="md:w-1/2 md:pr-12 flex justify-end order-1 md:order-1">
                <div class="w-12 h-12 rounded-full bg-green-600 border-4 border-green-100 flex items-center justify-center z-10">
                  <i class="fas fa-globe-asia text-white"></i>
                </div>
              </div>
              <div class="md:w-1/2 md:pl-12 md:text-left mb-4 md:mb-0 order-2 md:order-2">
                <h3 class="text-2xl font-bold text-green-600">2020年</h3>
                <p class="text-gray-600 mt-2">成立十周年，门店数量突破200家，产品远销30多个国家和地区</p>
              </div>
            </div>
          </div>
        </div>
      </div>
      
      <!-- 品质承诺 -->
      <div class="mb-20">
        <h2 class="text-3xl font-bold mb-8 text-center text-gray-800">品质承诺</h2>
        
        <div class="bg-white rounded-xl shadow-lg overflow-hidden">
          <div class="md:flex">
            <div class="md:w-1/3 bg-green-600 text-white p-8 flex items-center justify-center">
              <div class="text-center">
                <i class="fas fa-certificate text-5xl mb-4"></i>
                <h3 class="text-2xl font-bold">臻品质 · 臻生活</h3>
                <p class="mt-2 opacity-80">每一片茶叶，都凝聚着我们对品质的执着追求</p>
              </div>
            </div>
            <div class="md:w-2/3 p-8">
              <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <div class="flex items-start">
                  <div class="flex-shrink-0 mt-1">
                    <div class="w-8 h-8 rounded-full bg-green-100 flex items-center justify-center">
                      <i class="fas fa-leaf text-green-600"></i>
                    </div>
                  </div>
                  <div class="ml-4">
                    <h3 class="text-xl font-semibold mb-2 text-gray-800">优选原料</h3>
                    <p class="text-gray-600">精选优质茶区原料，从源头把控品质，确保每一片茶叶都来自最适宜的生长环境。</p>
                  </div>
                </div>
                
                <div class="flex items-start">
                  <div class="flex-shrink-0 mt-1">
                    <div class="w-8 h-8 rounded-full bg-green-100 flex items-center justify-center">
                      <i class="fas fa-flask text-green-600"></i>
                    </div>
                  </div>
                  <div class="ml-4">
                    <h3 class="text-xl font-semibold mb-2 text-gray-800">严格检测</h3>
                    <p class="text-gray-600">所有茶品均经过专业实验室多项检测，确保无农残、无添加，安全健康。</p>
                  </div>
                </div>
                
                <div class="flex items-start">
                  <div class="flex-shrink-0 mt-1">
                    <div class="w-8 h-8 rounded-full bg-green-100 flex items-center justify-center">
                      <i class="fas fa-medal text-green-600"></i>
                    </div>
                  </div>
                  <div class="ml-4">
                    <h3 class="text-xl font-semibold mb-2 text-gray-800">匠心制作</h3>
                    <p class="text-gray-600">传承传统制茶工艺，结合现代科技，每一款茶品都是匠心之作。</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      
      <!-- 团队介绍 -->
      <div class="mb-16">
        <h2 class="text-3xl font-bold mb-12 text-center text-gray-800">核心团队</h2>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div class="bg-white rounded-lg shadow-lg overflow-hidden hover:shadow-xl transition-shadow">
            <div class="h-64 overflow-hidden">
              <img src="https://tse3-mm.cn.bing.net/th/id/OIP-C.GEVmaEzBwI5QFjSNg-Sw9AHaE8?w=272&h=181&c=7&r=0&o=5&dpr=1.3&pid=1.7" 
                   alt="创始人" 
                   class="w-full h-full object-cover">
            </div>
            <div class="p-6">
              <h3 class="text-xl font-bold mb-1">王明远</h3>
              <p class="text-green-600 mb-4">创始人 & CEO</p>
              <p class="text-gray-600">福建安溪人，茶文化传承者，拥有20年制茶经验，国家级评茶师，致力于推广中国传统茶文化。</p>
            </div>
          </div>
          
          <div class="bg-white rounded-lg shadow-lg overflow-hidden hover:shadow-xl transition-shadow">
            <div class="h-64 overflow-hidden">
              <img src="https://tse3-mm.cn.bing.net/th/id/OIP-C.doiSpQSHTNXipcmjVTzmSQHaE7?w=241&h=180&c=7&r=0&o=5&dpr=1.3&pid=1.7" 
                   alt="茶艺总监" 
                   class="w-full h-full object-cover">
            </div>
            <div class="p-6">
              <h3 class="text-xl font-bold mb-1">林雨晴</h3>
              <p class="text-green-600 mb-4">茶艺总监</p>
              <p class="text-gray-600">国家高级茶艺师，曾获全国茶艺大赛金奖，负责公司茶艺培训与茶文化推广工作。</p>
            </div>
          </div>
          
          <div class="bg-white rounded-lg shadow-lg overflow-hidden hover:shadow-xl transition-shadow">
            <div class="h-64 overflow-hidden">
              <img src="https://tse2-mm.cn.bing.net/th/id/OIP-C.aGxHdIUw8m0CUBHJZLN7kwAAAA?w=211&h=189&c=7&r=0&o=5&dpr=1.3&pid=1.7" 
                   alt="产品研发总监" 
                   class="w-full h-full object-cover">
            </div>
            <div class="p-6">
              <h3 class="text-xl font-bold mb-1">张志远</h3>
              <p class="text-green-600 mb-4">产品研发总监</p>
              <p class="text-gray-600">农学博士，专注茶叶种植与加工研究15年，带领团队不断创新茶品种类与工艺。</p>
            </div>
          </div>
        </div>
      </div>
      
      <!-- 联系我们 -->
      <div class="text-center mb-16">
        <h2 class="text-3xl font-bold mb-6 text-gray-800">加入我们的茶文化之旅</h2>
        <p class="text-gray-600 max-w-2xl mx-auto mb-8">无论您是茶文化爱好者，还是寻求商务合作的伙伴，我们都期待与您相遇</p>
        <router-link to="/contact" class="bg-green-600 hover:bg-green-700 text-white font-bold py-3 px-8 rounded-lg transition duration-300 inline-block">
          联系我们
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutPage'
}
</script>