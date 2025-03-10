<template>
  <footer class="bg-gray-900 text-gray-300 py-12">
    <div class="container mx-auto px-4">
      <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
        <div>
          <h3 class="text-white text-lg font-bold mb-4">联系我们</h3>
          <p class="mb-2">客服热线：400-888-8888</p>
          <p class="mb-2">邮箱：service@tea.com</p>
          <p>地址：北京市朝阳区茶香路 88 号</p>
        </div>
        <div>
          <h3 class="text-white text-lg font-bold mb-4">快速链接</h3>
          <ul class="space-y-2">
            <li><a href="#" class="hover:text-white">加盟合作</a></li>
            <li><a href="#" class="hover:text-white">招贤纳士</a></li>
            <li><a href="#" class="hover:text-white">服务条款</a></li>
          </ul>
        </div>
        <div>
          <h3 class="text-white text-lg font-bold mb-4">关注我们</h3>
          <div class="flex space-x-4">
            <a href="#" class="hover:text-white"><i class="fab fa-weixin text-2xl"></i></a>
            <a href="#" class="hover:text-white"><i class="fab fa-weibo text-2xl"></i></a>
            <a href="#" class="hover:text-white"><i class="fab fa-instagram text-2xl"></i></a>
          </div>
        </div>
        <div>
          <img src="https://ai-public.mastergo.com/ai/img_res/b3568bcf313d8433b95595a82095db47.jpg" 
               alt="微信二维码"
               class="w-32">
          <p class="mt-2">扫码关注公众号</p>
        </div>
      </div>
      <div class="border-t border-gray-800 mt-8 pt-8 text-center">
        <p>© 2024 臻茗茶业 版权所有</p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'FooterComponent'
}
</script>