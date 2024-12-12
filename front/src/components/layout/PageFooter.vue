<script lang="ts" setup></script>
<template>
  <div class="page-footer">
    <div class="links">
      <a class="link" href="https://www.trimps.ac.cn/gass/index.html" target="_blank">GyoiThonPlus</a>
    </div>
    <div class="copyright">
      Copyright
      <CopyrightOutlined class="icon-copyright" /> 2024 GyoiThonPlus based on Gyoithon
    </div>
  </div>
</template>

<style scoped lang="less">
  .page-footer {
    text-align: center;
    @apply text-gray-400;

    .links {
      display: flex;
      justify-content: center;

      .link {
        @apply hover:text-gray-400 pl-4 pr-4;
      }
    }

    .copyright {
      margin-top: 8px;

      .icon-copyright {
        margin: 0;
      }
    }
  }
</style>
