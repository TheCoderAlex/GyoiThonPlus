<script lang="ts" setup>
  import { GithubFilled } from '@ant-design/icons-vue';
  import { useRouter } from 'vue-router';

  const router = useRouter();
  function getIn() {
    router.push('/workplace');
  }
</script>
<template>
  <div class="home text-center flex flex-col justify-center">
    <div class="transform w-full">
      <div class="tracking-wide slogan text-[3.5rem] xl:text-[5.25rem] font-extralight">
        GyoiThonPlus
      </div>
      <p class="text-subtext text-[1.5rem] xl:text-[1.75rem] font-extralight tracking-wide">
        Automated Penetration Testing Tool Based on Artificial Intelligence
      </p>
      <button
        @click="getIn"
        class="bg-primary-300 hover:bg-primary-400 cursor-pointer mt-lg shadow border-0 outline-none text-xl px-[64px] py-lg rounded-sm"
      >
        Let's Go!
      </button>
      <br />
<!--      <div class="inline-block text-gray-200 text-xl mr-lg">Powered by:</div>-->
<!--      <div class="powered-by-list inline-flex mt-xl text-subtext">-->
<!--        <a href="https://www.antdv.com/" target="_blank" class="powered-by text-subtext hover:text-text cursor-pointer">-->
<!--          <img class="w-6" src="@/assets/logo/antdv.svg" />-->
<!--          antd design vue-->
<!--        </a>-->
<!--        <a-->
<!--          href="https://tailwindcss.com/"-->
<!--          target="_blank"-->
<!--          class="powered-by text-subtext mx-md hover:text-text cursor-pointer"-->
<!--        >-->
<!--          <img class="w-6" src="@/assets/logo/tailwindcss.svg" />-->
<!--          tailwindcss-->
<!--        </a>-->
<!--        <a href="http://www.vitejs.net/" target="_blank" class="powered-by text-subtext hover:text-text cursor-pointer">-->
<!--          <img class="w-5" src="@/assets/vite.svg" />-->
<!--          vitejs-->
<!--        </a>-->
<!--      </div>-->
    </div>
  </div>
</template>
<style scoped lang="less">
  .home {
    min-height: max(100vh, 600px);
    margin-top: -78px;
  }
</style>
