<template>
  <div class="home">
    <header>
      <div class="header container">
        <div class="left">
          <div class="tel">
            <i class="el-icon-phone-outline"></i>
            <span>+86-20-38383032</span>
          </div>
          <div class="mail">
            <i class="el-icon-message"></i>
            <span>support@bosslog.cn</span>
          </div>
        </div>
        <div class="center">
          <div class="lang">
            <el-select v-model="lang">
              <el-option v-for="item in langList" :key="item.value" :label="item.label" :value="item.value">
              </el-option>
            </el-select>
          </div>
          <div class="site">
            <el-select v-model="site">
              <el-option v-for="item in siteList" :key="item.value" :label="item.label" :value="item.value">
              </el-option>
            </el-select>
          </div>
        </div>
        <div class="right">
          <div class="account">
            <el-button type="primary" plain icon="el-icon-monitor">我的账户</el-button>
          </div>
          <div class="register">
            <el-button type="primary" icon="el-icon-monitor">免费注册</el-button>
          </div>
        </div>
      </div>
    </header>

    <main>
      <nav>
        <div class="nav container">
          <div class="logo">
            <img src="../assets/boss_logo.png" />
          </div>
          <div class="menu">
            <el-menu default-active="1" mode="horizontal">
              <el-menu-item index="1">首页</el-menu-item>
              <el-menu-item index="2">即时运价</el-menu-item>
              <el-menu-item index="3">在线订舱</el-menu-item>
              <el-menu-item index="4">SO查询</el-menu-item>
              <el-menu-item index="5">提单补料</el-menu-item>
              <el-menu-item index="6">账单发票</el-menu-item>
              <el-menu-item index="7">货物跟踪</el-menu-item>
              <el-menu-item index="8">关于博森</el-menu-item>
              <el-menu-item index="9">联系我们</el-menu-item>
            </el-menu>
          </div>
        </div>
      </nav>
    </main>
  </div>
</template>

<script>
export default {
  data() {
    return {
      lang: 'zh',
      langList: [
        { value: 'zh', label: '中文' },
        { value: 'en', label: 'English' }
      ],
      site: 'colombia',
      siteList: [
        { value: 'china', label: '中国' },
        { value: 'colombia', label: '哥伦比亚' }
      ]
    }
  }
}
</script>

<style lang="scss">
.home {
  min-height: calc(100vh - 70px);
  .container {
    max-width: 1190px;
    margin: 0 auto;
  }

  header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    background-color: #999;
    .header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 70px;
      .left {
        display: flex;
        > div {
          margin-right: 20px;
          color: #fff;
          cursor: pointer;
        }
      }
      .center {
        flex: 1;
        display: flex;
        > div {
          width: 120px;
          margin-right: 20px;
        }
      }
      .right {
        display: flex;
        .account {
          margin-right: 20px;
        }
      }
    }
  }

  main {
    margin-top: 70px;
    nav {
      .nav {
        display: flex;
        .logo {
          width: 120px;
        }
        .menu {
          flex: 1;
        }
      }
    }
  }
}
</style>
