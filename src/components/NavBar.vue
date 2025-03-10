<template>
  <nav class="fixed top-0 left-0 right-0 z-50 bg-white/95 backdrop-blur-sm shadow-md dark:bg-gray-800/95 dark:shadow-gray-900/20 transition-colors duration-300">
    <div class="container mx-auto px-4">
      <div class="flex items-center justify-between h-16">
        <div class="flex items-center">
          <img src="https://ai-public.mastergo.com/ai/img_res/8272625579ca0e6b4cd2f4aed2d355d9.jpg" 
               alt="茶品logo" 
               class="h-10">
        </div>
        
        <div class="hidden md:flex items-center space-x-8">
          <router-link to="/" class="nav-link dark:text-gray-200 dark:hover:text-green-400">首页</router-link>
          <router-link to="/products" class="nav-link dark:text-gray-200 dark:hover:text-green-400">产品系列</router-link>
          <router-link to="/stores" class="nav-link dark:text-gray-200 dark:hover:text-green-400">门店查询</router-link>
          <router-link to="/about" class="nav-link dark:text-gray-200 dark:hover:text-green-400">关于我们</router-link>
        </div>

        <div class="flex items-center space-x-4">
          <button @click="toggleTheme" class="theme-btn !rounded-button">
            <i :class="isDarkMode ? 'fas fa-sun' : 'fas fa-moon'" class="mr-2"></i>
            {{ isDarkMode ? '日间模式' : '夜间模式' }}
          </button>
          <a href="tel:400-888-8888" class="contact-btn !rounded-button dark:bg-green-700 dark:hover:bg-green-800">
            <i class="fas fa-phone-alt mr-2"></i>
            400-888-8888
          </a>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'NavBar',
  data() {
    return {
      isDarkMode: false
    }
  },
  mounted() {
    // 从localStorage中获取主题设置
    const savedTheme = localStorage.getItem('theme');
    if (savedTheme === 'dark') {
      this.isDarkMode = true;
      document.documentElement.classList.add('dark');
    }
  },
  methods: {
    toggleTheme() {
      this.isDarkMode = !this.isDarkMode;
      if (this.isDarkMode) {
        document.documentElement.classList.add('dark');
        localStorage.setItem('theme', 'dark');
      } else {
        document.documentElement.classList.remove('dark');
        localStorage.setItem('theme', 'light');
      }
    }
  }
}
</script>

<style scoped>
.nav-link {
  color: #374151;
  font-weight: 500;
  position: relative;
  padding-bottom: 2px;
  transition: color 0.3s ease;
}

.nav-link:hover {
  color: #047857;
}

.nav-link::after {
  content: '';
  position: absolute;
  width: 0;
  height: 2px;
  bottom: -2px;
  left: 0;
  background-color: #047857;
  transition: width 0.3s ease;
}

.nav-link:hover::after {
  width: 100%;
}

.dark .nav-link::after {
  background-color: #10b981;
}

.theme-btn {
  padding: 0.5rem 1rem;
  background-color: #f3f4f6;
  color: #374151;
  font-weight: 500;
  border-radius: 0.5rem;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05);
  transition: all 0.3s ease;
}

.theme-btn:hover {
  background-color: #e5e7eb;
  transform: translateY(-1px);
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
}

.dark .theme-btn {
  background-color: #4b5563;
  color: #e5e7eb;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.2);
}

.dark .theme-btn:hover {
  background-color: #374151;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.3);
}

.contact-btn {
  padding: 0.5rem 1rem;
  background-color: #047857;
  color: white;
  font-weight: 500;
  border-radius: 0.5rem;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
}

.contact-btn:hover {
  background-color: #065f46;
  transform: translateY(-1px);
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
</style>