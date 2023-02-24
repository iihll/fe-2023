<script setup>
import html2pdf from 'html2pdf.js'

const handleCLick = () => {
  html2pdf(document.querySelector('.container'), { filename: 'resume.pdf' })
}
</script>

<template>
  <button @click="handleCLick">download pdf</button>
  <div class="container">
    <div class="base-info">
      <div>姓名：邢端清</div>
      <div>年龄：26</div>
      <div>电话：18735363391</div>
      <div>邮箱：52966149@qq.com</div>
    </div>

    <div class="edu">
      <div class="title">教育经历</div>
      <div class="main">
        <div>山西工程技术学院 本科（统招）</div>
        <div>计算机科学与技术</div>
        <div>2018.9 - 2020.6</div>
      </div>
    </div>

    <div class="skills">
      <div class="title">专业技能</div>

      <div class="skill-list">
        <div>
          1. 熟练使用原生 JavaScript 以及常用 JavaScript 库，如
          lodash、Echarts、axios、Ant-design，Element-UI
          等，快速实现响应式网页的开发。
        </div>

        <div>
          2. 有 JS 性能优化实践经验；熟练使用 ES6
          及更高版本发布的语言特性和语法。
        </div>
        <div>
          3. 熟练使用 Vue
          全家桶进行单页应用开发，并对其源码有认识和了解，有完整的项目开发经验。
        </div>
        <div>4. 熟练使用 uni-app 及相关生态进行移动端小程序、H5的开发。</div>
        <div>5. 能够使用 React 全家桶进行开发，并有实战经验。</div>
        <div>
          6. 熟练使用 Git
          版本工具进行代码控制与协作；能手动部署前端项目，并能完成自动化部署，了解
          Linux 的使用。
        </div>
      </div>
    </div>

    <div class="work">
      <div class="title">工作经历</div>

      <div class="item">
        <div class="info">
          <div>牛创新能源自游家汽车 </div>
          <div>中级前端开发工程师</div>
          <div>2022.4 - 2022.12</div>
        </div>

        <div class="content">
          <div>1. 负责自游家汽车 C 端产品功能的前端开发与管理工作。</div>
          <div>2. 产品需求评审、测试用例评审、跨部门工作协调。</div>
          <div>3. 根据产品需求难点进行技术调研。</div>
          <div>4. 参与产品前端技术选型与开发规范的制定。</div>
          <div>5. 完成测试、验收过程中的 bug 修复。</div>
        </div>
      </div>

      <div class="item">
        <div class="info">
          <div>百融云创科技股份有限公司</div>
          <div>初级前端开发工程师</div>
          <div>2020.4 - 2022.4</div>
        </div>

        <div class="content">
          <div>1. 负责部门核心项目从零到一的开发和维护工作。</div>
          <div>
            2.
            负责项目技术难点的调研和解决，组织人员进行私有流程图库的封装和维护。
          </div>
          <div>
            3. 设计并不断优化调整项目的架构组织，模块划分，代码
            review，保证项目功能达标和成员能充分的了解项目代码组织，对项目有持续更新的认识。
          </div>
        </div>
      </div>
    </div>

    <div class="prj">
      <div class="title">项目经历</div>

      <div class="item">
        <div class="info">
          <div>自游家汽车C端小程序 H5</div>
          <div>牛创新能源自游家汽车</div>
          <div>2022.4 - 2022.12</div>
        </div>

        <div class="content">
          <div>项目描述：</div>
          <div>
            自游家汽车小程序，H5，是自游家汽车给购车用户提供浏览、车辆选配、购车支付、门店查找等一系列
            NIUTRON
            汽车相关服务的平台，新车发布会稳定上线运行并实现累计3W+订单支付，支持业务方完成相关工作。
          </div>
          <div>技术要点：</div>
          <div>
            1. 采用 Vue 全家桶、uni-app、uview，使项目快速成型投产使用。
          </div>
          <div>2. 封装自定义组件：购车选配流程及页面动效组件。</div>
          <div>3. 一体化多端登录数据共享；三方支付跳转。</div>
          <div>4. H5 内嵌 APP 与原生之间通信完成业务要求。</div>
          <div>5. 规范接口文档，接口错误处理规范。提高了前后端联调的效率。</div>
          <div>项目职责：</div>
          <div>1. 负责整个项目前端部分的开发与管理工作。</div>
          <div>2. 负责需求评审、技术选型、代码设计与代码开发的工作。</div>
          <div>3. 负责 H5 打通 APP 通信与相关开发人员沟通联调。</div>
        </div>
      </div>

      <div class="item">
        <div class="info">
          <div>策略营销引擎</div>
          <div>百融云创科技股份有限公司</div>
          <div>2021.4 - 2022.4</div>
        </div>

        <div class="content">
          <div>项目描述：</div>
          <div>
            策略营销引擎是公司确定营销方向后，从零开发的一款主要针对大银行客户的精准策略营销的中后台管理项目，以流程图托拉拽的方式，完成营销流程中的客群筛选、活动配置、渠道协同、素材定义、策略评估等灵活的配置。
          </div>
          <div>技术要点：</div>
          <div>1. 采用 Vue3 全家桶、UXD-UI、VIX，使项目快速成型投产使用。</div>
          <div>2. 封装自定义组件：流程图拖拉拽，规则筛选拖拉拽组件。</div>
          <div>
            3. 采用树形结构 + 递归的封装形式，提供了一套各个组件之间关系维护。
          </div>
          <div>
            4. 封装自定义 hooks，配合自定义组件，提升列表页 80% 的开发效率。
          </div>
          <div>5. 规范接口文档，接口错误处理规范。提高了前后端联调的效率。</div>
          <div>项目职责：</div>
          <div>1. 负责整个项目前端部分的开发与管理工作。</div>
          <div>2. 负责需求评审、技术选型、代码设计与代码开发的工作。</div>
          <div>
            3.
            负责部门基础业务组件库的开发工作，业务组件库包含路由、系统状态、基础布局、自定义
            hooks、常用工具类、规范请求及业务常用组件，业务组件库已在部门两个项目上实际落地，大大提高了项目的整体开发效率与质量。
          </div>
        </div>
      </div>

      <div class="item">
        <div class="info">
          <div>存储数据管理平台</div>
          <div>百融云创科技股份有限公司</div>
          <div>2020.4 - 2021.4</div>
        </div>

        <div class="content">
          <div>项目描述：</div>
          <div>
            数据存储管理的可视化平台，是集分析、图表、存储数据可视化、存储数据上传与下载、存储池购买与管理为一体的存储管理平台。
          </div>
          <div>技术要点：</div>
          <div>
            1. 采用 Vue 全家桶、Element-ui、Echarts，使项目快速成型投产使用。
          </div>
          <div>
            2. 采用队列数据结构及 JS 异步编程与 Axios
            封装上传下载组件，赋予冷存储系统上传暂停、取消、限制并行上传下载数，进度展示与搜索的功能。
          </div>
          <div>
            3. 采用 Electron 和 Websocket
            开发冷存储平台归档软件桌面平台，解决浏览器下载内存占用过大浏览器页面崩溃的问题与跨平台下载。
          </div>
          <div>项目职责：</div>
          <div>1. 负责冷存储平台上传下载队列的开发与维护。</div>
          <div>2. 负责存储池数据可视化的开发。</div>
          <div>
            3.
            负责附属大文件下载工具归档软件从零到一的开发，参与需求评审、代码设计与代码开发的工作。
          </div>
        </div>
      </div>

      <div class="item">
        <div class="info">
          <div>数据治理平台</div>
          <div>百融云创科技股份有限公司</div>
          <div>2020.4 - 2020.12</div>
        </div>

        <div class="content">
          <div>项目描述：</div>
          <div>
            数据治理平台是一款数据关系描述、数据规范管理、数据质量校验、数据安全及数据集成于一体的中后台大数据管理平台。
          </div>
          <div>技术要点：</div>
          <div>1. 采用 React16 + Dvajs + Ant-design 搭建项目。</div>
          <div>
            2. 基于 Antd-G6 二次封装，完成数据调度及数据脚本的可视化操作与管理。
          </div>
          <div>项目职责：</div>
          <div>
            1.
            负责项目数据调度流程图、数据源管理及数据服务管理的代码开发与迭代版本维护工作。
          </div>
          <div>
            2.
            负责前端性能优化，完成代码层面及打包层面的优化，减少冗余代码，提升生产打包后的页面加载速度。
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  width: 220mm;
  min-height: 297mm;
  padding: 10mm;
  padding-right: 20mm;
  background: white;
}

.base-info {
  display: flex;
  flex-wrap: wrap;
  font-size: 16px;
}

.base-info div {
  width: 50%;
}

.edu {
  .main {
    display: flex;

    div {
      flex: 1;
    }
  }
}

.skills {
  .skill-list {
    line-height: 24px;
  }
}

.work {
  .item {
    margin-bottom: 12px;

    .info {
      display: flex;
      margin-bottom: 12px;

      div {
        flex: 1;
      }
    }

    .content {
      line-height: 24px;
    }
  }
}

.prj {
  .item {
    margin-bottom: 12px;

    .info {
      display: flex;
      margin-bottom: 12px;

      div {
        flex: 1;
      }
    }

    .content {
      line-height: 24px;
    }
  }
}

.title {
  display: flex;
  align-items: center;
  font-size: 24px;
  font-weight: bold;
  background-color: lightblue;
  color: white;
  border-radius: 12px;
  padding: 4px 4px 8px;
  margin: 12px 0;
}
</style>
