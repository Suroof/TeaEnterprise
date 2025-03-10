<template>
  <div class="contact min-h-screen pt-16">
    <div class="bg-green-600 text-white py-12">
      <div class="container mx-auto px-4">
        <h1 class="text-4xl font-bold text-center mb-6">联系我们</h1>
        <p class="text-center text-lg mb-8">我们期待听到您的声音，随时为您提供帮助和支持</p>
      </div>
    </div>
    
    <!-- 联系信息卡片 -->
    <div class="container mx-auto px-4 py-12">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-12">
        <div class="bg-white rounded-lg shadow-lg p-8 text-center hover:shadow-xl transition-shadow">
          <div class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mx-auto mb-6">
            <i class="fas fa-map-marker-alt text-green-600 text-2xl"></i>
          </div>
          <h3 class="text-xl font-bold mb-4">公司地址</h3>
          <p class="text-gray-600">北京市朝阳区茶香路88号</p>
          <p class="text-gray-600 mt-2">臻茗茶业大厦</p>
        </div>
        
        <div class="bg-white rounded-lg shadow-lg p-8 text-center hover:shadow-xl transition-shadow">
          <div class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mx-auto mb-6">
            <i class="fas fa-phone-alt text-green-600 text-2xl"></i>
          </div>
          <h3 class="text-xl font-bold mb-4">联系电话</h3>
          <p class="text-gray-600">客服热线：400-888-8888</p>
          <p class="text-gray-600 mt-2">商务合作：010-12345678</p>
        </div>
        
        <div class="bg-white rounded-lg shadow-lg p-8 text-center hover:shadow-xl transition-shadow">
          <div class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mx-auto mb-6">
            <i class="fas fa-envelope text-green-600 text-2xl"></i>
          </div>
          <h3 class="text-xl font-bold mb-4">电子邮箱</h3>
          <p class="text-gray-600">客户服务：service@tea.com</p>
          <p class="text-gray-600 mt-2">商务合作：business@tea.com</p>
        </div>
      </div>
      
      <!-- 联系表单 -->
      <div class="max-w-4xl mx-auto bg-white rounded-lg shadow-lg overflow-hidden">
        <div class="md:flex">
          <div class="md:w-1/2 bg-green-600 text-white p-8 flex flex-col justify-center">
            <h2 class="text-3xl font-bold mb-6">与我们取得联系</h2>
            <p class="mb-6 leading-relaxed">无论您有任何问题、建议或合作意向，都欢迎通过表单联系我们。我们的团队将在24小时内回复您。</p>
            <div class="space-y-4">
              <div class="flex items-center">
                <i class="fas fa-clock mr-4 text-xl"></i>
                <span>工作时间：周一至周日 9:00-18:00</span>
              </div>
              <div class="flex items-center">
                <i class="fas fa-users mr-4 text-xl"></i>
                <span>专业团队，为您提供一对一服务</span>
              </div>
              <div class="flex items-center">
                <i class="fas fa-headset mr-4 text-xl"></i>
                <span>7×24小时在线客服支持</span>
              </div>
            </div>
          </div>
          
          <div class="md:w-1/2 p-8">
            <form>
              <div class="mb-6">
                <label for="name" class="block text-gray-700 font-medium mb-2">您的姓名</label>
                <input 
                  type="text" 
                  id="name" 
                  class="w-full px-4 py-3 border rounded-lg focus:outline-none focus:ring-2 focus:ring-green-500"
                  placeholder="请输入您的姓名"
                >
              </div>
              
              <div class="mb-6">
                <label for="email" class="block text-gray-700 font-medium mb-2">电子邮箱</label>
                <input 
                  type="email" 
                  id="email" 
                  class="w-full px-4 py-3 border rounded-lg focus:outline-none focus:ring-2 focus:ring-green-500"
                  placeholder="请输入您的电子邮箱"
                >
              </div>
              
              <div class="mb-6">
                <label for="subject" class="block text-gray-700 font-medium mb-2">主题</label>
                <select 
                  id="subject" 
                  class="w-full px-4 py-3 border rounded-lg focus:outline-none focus:ring-2 focus:ring-green-500"
                >
                  <option value="">请选择咨询主题</option>
                  <option value="product">产品咨询</option>
                  <option value="order">订单问题</option>
                  <option value="cooperation">商务合作</option>
                  <option value="suggestion">意见建议</option>
                  <option value="other">其他问题</option>
                </select>
              </div>
              
              <div class="mb-6">
                <label for="message" class="block text-gray-700 font-medium mb-2">留言内容</label>
                <textarea 
                  id="message" 
                  rows="5" 
                  class="w-full px-4 py-3 border rounded-lg focus:outline-none focus:ring-2 focus:ring-green-500"
                  placeholder="请详细描述您的问题或需求"
                ></textarea>
              </div>
              
              <button 
                type="submit" 
                class="w-full bg-green-600 hover:bg-green-700 text-white font-bold py-3 px-6 rounded-lg transition duration-300"
              >
                提交留言
              </button>
            </form>
          </div>
        </div>
      </div>
      
      <!-- 常见问题 -->
      <div class="mt-16">
        <h2 class="text-3xl font-bold text-center mb-12">常见问题</h2>
        <div class="max-w-4xl mx-auto grid grid-cols-1 md:grid-cols-2 gap-8">
          <div class="bg-white p-6 rounded-lg shadow-md hover:shadow-lg transition-shadow">
            <h3 class="text-xl font-bold mb-3 flex items-center">
              <i class="fas fa-question-circle text-green-600 mr-3"></i>
              如何选择适合自己的茶叶？
            </h3>
            <p class="text-gray-600">选择茶叶可以根据个人口味偏好、季节和功效需求。我们提供专业的茶叶推荐服务，您可以在门店或线上咨询我们的茶艺师。</p>
          </div>
          
          <div class="bg-white p-6 rounded-lg shadow-md hover:shadow-lg transition-shadow">
            <h3 class="text-xl font-bold mb-3 flex items-center">
              <i class="fas fa-question-circle text-green-600 mr-3"></i>
              茶叶保质期是多久？
            </h3>
            <p class="text-gray-600">不同茶叶保质期不同，一般绿茶保存期为1年，乌龙茶2-3年，红茶3-5年，普洱茶则可以长期存放且越陈越香。</p>
          </div>
          
          <div class="bg-white p-6 rounded-lg shadow-md hover:shadow-lg transition-shadow">
            <h3 class="text-xl font-bold mb-3 flex items-center">
              <i class="fas fa-question-circle text-green-600 mr-3"></i>
              如何正确冲泡茶叶？
            </h3>
            <p class="text-gray-600">不同茶叶有不同的冲泡方法，包括水温、时间和器具选择。我们的产品包装上有详细的冲泡指南，您也可以参考我们网站上的茶艺教程。</p>
          </div>
          
          <div class="bg-white p-6 rounded-lg shadow-md hover:shadow-lg transition-shadow">
            <h3 class="text-xl font-bold mb-3 flex items-center">
              <i class="fas fa-question-circle text-green-600 mr-3"></i>
              如何成为会员？
            </h3>
            <p class="text-gray-600">您可以在我们的官网、APP或任意门店注册成为会员，享受积分奖励、生日礼遇、新品尝鲜等多重会员权益。</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContactUsPage'
}
</script>