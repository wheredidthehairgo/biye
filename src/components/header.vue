<template>
	<header>
		<a v-link="{name: 'index'}" class="brand">
      <span>数字内容处理及安全性应用实验室</span>
    </a>
		<ul class="navbar">
			<li><a v-link="{name: 'index'}">首页</a></li>
			<li><a v-link="{name: 'login'}">实验室概况</a></li>
      <li><a v-link="{name: 'login'}">科学研究</a></li>
      <li><a v-link="{name: 'login'}">队伍建设</a></li>
      <li><a v-link="{name: 'login'}">开放交流</a></li>
      <li><a v-link="{name: 'login'}">运行管理</a></li>
      <li><a v-link="{name: 'login'}">人才培养</a></li>
      <li><a v-link="{name: 'login'}">开放交流</a></li>
		</ul>
	</header>
</template>

<script>
  import {
    changeToken,
    checkToken,
    fetchUser,
    fetchCollection,
    fetchMsgCount,
    delToken,
    changeLoginUser,
  } from '../vuex/actions';
  import { getMsgCount, getToken } from '../vuex/getters';
  export default {
    vuex: {
      actions: {
        changeToken,
        checkToken,
        fetchUser,
        fetchCollection,
        fetchMsgCount,
        delToken,
        changeLoginUser,
      },
      getters: {
        token: getToken,
        msgCount: getMsgCount,
      },
    },
  };
</script>

<style lang="scss" scoped>
  header {
    overflow: hidden;
    background-color: #72c1f8;
    padding: 0 5%;
    margin-bottom: 20px;
  }

  .brand {
    float: left;
    width: 240pxpx;
    height: 30px;
    padding: 5px 20px;
    span {
      color: #FFF;
    }
  }

  .navbar {
    float: right;
    overflow: hidden;
    display: block;

    li {
      float: left;
    }

    a {
      font-size: 13px;
      display: block;
      padding: .5em;
      color: #FFF;
    }
  }

  .h {
    background-color: #80BD01;
    height: 14px;
    min-width: 14px;
    padding: 0 2px;
    padding-top: 1px;
    margin-left: 1px;
    display: inline-block;
    font-size: 10px;
    line-height: 14px;
    text-align: center;
    border-radius: 10px;
    color: #FFF;
  }

  @media (max-width: 400px) {
    .brand {
      float: none;
      margin: 0 auto;
      display: block;
      text-align: center;
    }

    .navbar {
      float: none;
      text-align: center;

      li {
        float: none;
        display: inline-block;
      }
    }
  }

  @media (max-width: 512px) {
    .brand {
      span {
        font-size: 16px;
      }
    }
  }
</style>
