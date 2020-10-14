

### 目录
<!-- TOC -->
| 序号. | 问题 |
| --- | --------- |
| | [Core React](#core-react) |
|1 | [什么是 React?](#什么是-react) |
|2 | [React 的主要特点是什么?](#react-的主要特点是什么) |
|3 | [什么是 JSX?](#什么是-jsx) |
|4 | [元素和组件有什么区别?](#元素和组件有什么区别) |
|5 | [如何在 React 中创建组件?](#如何在-react-中创建组件) |
|6 | [何时使用类组件和函数组件?](#何时使用类组件和函数组件) |
|7 | [什么是 Pure Components?](#什么是-pure-components) |
|8 | [React 的状态是什么?](#react-的状态是什么) |
|9 | [React 中的 props 是什么?](#react-中的-props-是什么) |
|10 | [状态和属性有什么区别?](#状态和属性有什么区别) |
|11 | [我们为什么不能直接更新状态?](#我们为什么不能直接更新状态) |
|12 | [回调函数作为 `setState()` 参数的目的是什么?](#回调函数作为-setstate-参数的目的是什么) |
|13 | [HTML 和 React 事件处理有什么区别?](#html-和-react-事件处理有什么区别) |
|14 | [如何在 JSX 回调中绑定方法或事件处理程序?](#如何在-jsx-回调中绑定方法或事件处理程序) |
|15 | [如何将参数传递给事件处理程序或回调函数?](#如何将参数传递给事件处理程序或回调函数) |
|16 | [React 中的合成事件是什么?](#react-中的合成事件是什么) |
|17 | [什么是内联条件表达式?](#什么是内联条件表达式) |
|18 | [什么是 "key" 属性，在元素数组中使用它们有什么好处?](#什么是-key-属性在元素数组中使用它们有什么好处) |
|19 | [refs 有什么用?](#refs-有什么用) |
|20 | [如何创建 refs?](#如何创建-refs) |
|21 | [什么是 forward refs?](#什么是-forward-refs) |
|22 | [callback refs 和 findDOMNode() 哪一个是首选选项?](#callback-refs-和-finddomnode-哪一个是首选选项) |
|23 | [为什么 String Refs 被弃用?](#为什么-string-refs-被弃用) |
|24 | [什么是 Virtual DOM?](#什么是-virtual-dom) |
|25 | [Virtual DOM 如何工作?](#virtual-dom-如何工作) |
|26 | [Shadow DOM 和 Virtual DOM 之间有什么区别?](#shadow-dom-和-virtual-dom-之间有什么区别) |
|27 | [什么是 React Fiber?](#什么是-react-fiber) |
|28 | [React Fiber 的主要目标是什么?](#react-fiber-的主要目标是什么) |
|29 | [什么是受控组件?](#什么是受控组件) |
|30 | [什么是非受控组件?](#什么是非受控组件) |
|31 | [createElement 和 cloneElement 有什么区别?](#createelement-和-cloneelement-有什么区别) |
|32 | [在 React 中的提升状态是什么?](#在-react-中的提升状态是什么) |
|33 | [组件生命周期的不同阶段是什么?](#组件生命周期的不同阶段是什么) |
|34 | [React 生命周期方法有哪些?](#react-生命周期方法有哪些) |
|35 | [什么是高阶组件（HOC）?](#什么是高阶组件hoc) |
|36 | [如何为高阶组件创建属性代理?](#如何为高阶组件创建属性代理) |
|37 | [什么是上下文（Context）?](#什么是上下文context) |
|38 | [children 属性是什么?](#children-属性是什么) |
|39 | [怎样在 React 中写注释?](#怎样在-react-中写注释) |
|40 | [构造函数使用带 props 参数的目的是什么?](#构造函数使用带-props-参数的目的是什么) |
|41 | [什么是调解?](#什么是调解) |
|42 | [如何使用动态属性名设置 state ?](#如何使用动态属性名设置-state-) |
|43 | [每次组件渲染时调用函数的常见错误是什么?](#每次组件渲染时调用函数的常见错误是什么) |
|44 | [为什么有组件名称要首字母大写?](#为什么有组件名称要首字母大写) |
|45 | [为什么 React 使用 `className` 而不是 `class` 属性?](#为什么-react-使用-classname-而不是-class-属性) |
|46 | [什么是 Fragments ?](#什么是-fragments-) |
|47 | [为什么使用 Fragments 比使用容器 div 更好?](#为什么使用-fragments-比使用容器-div-更好) |
|48 | [在 React 中什么是 Portal ?](#在-react-中什么是-portal-) |
|49 | [什么是无状态组件?](#什么是无状态组件) |
|50 | [什么是有状态组件?](#什么是有状态组件) |
|51 | [在 React 中如何校验 props 属性?](#在-react-中如何校验-props-属性) |
|52 | [React 的优点是什么?](#react-的优点是什么) |
|53 | [React 的局限性是什么?](#react-的局限性是什么) |
|54 | [在 React v16 中的错误边界是什么?](#在-react-v16-中的错误边界是什么) |
|55 | [在 React v15 中如何处理错误边界?](#在-react-v15-中如何处理错误边界) |
|56 | [静态类型检查推荐的方法是什么?](#静态类型检查推荐的方法是什么) |
|57 | [`react-dom` 包的用途是什么?](#react-dom-包的用途是什么) |
|58 | [`react-dom` 中 render 方法的目的是什么?](#react-dom-中-render-方法的目的是什么) |
|59 | [ReactDOMServer 是什么?](#reactdomserver-是什么) |
|60 | [在 React 中如何使用 innerHTML?](#在-react-中如何使用-innerhtml) |
|61 | [如何在 React 中使用样式?](#如何在-react-中使用样式) |
|62 | [在 React 中事件有何不同?](#在-react-中事件有何不同) |
|63 | [如果在构造函数中使用 `setState()` 会发生什么?](#如果在构造函数中使用-setstate-会发生什么) |
|64 | [索引作为键的影响是什么?](#索引作为键的影响是什么) |
|65 | [在 `componentWillMount()` 方法中使用 `setState()` 好吗?](#在-componentwillmount-方法中使用-setstate-好吗) |
|66 | [如果在初始状态中使用 props 属性会发生什么?](#如果在初始状态中使用-props-属性会发生什么) |
|67 | [如何有条件地渲染组件?](#如何有条件地渲染组件) |
|68 | [为什么在 DOM 元素上展开 props 需要小心?](#为什么在-dom-元素上展开-props-需要小心) |
|69 | [在 React 中如何使用装饰器?](#在-react-中如何使用装饰器) |
|70 | [如何 memoize（记忆）组件?](#如何-memoize记忆组件) |
|71 | [如何实现 Server Side Rendering 或 SSR?](#如何实现-server-side-rendering-或-ssr) |
|72 | [如何在 React 中启用生产模式?](#如何在-react-中启用生产模式) |
|73 | [什么是 CRA 及其好处?](#什么是-cra-及其好处) |
|74 | [在 mounting 阶段生命周期方法的执行顺序是什么?](#在-mounting-阶段生命周期方法的执行顺序是什么) |
|75 | [在 React v16 中，哪些生命周期方法将被弃用?](#在-react-v16-中哪些生命周期方法将被弃用) |
|76 | [生命周期方法 `getDerivedStateFromProps()` 的目的是什么?](#生命周期方法-getderivedstatefromprops-的目的是什么) |
|77 | [生命周期方法 `getSnapshotBeforeUpdate()` 的目的是什么?](#生命周期方法-getsnapshotbeforeupdate-的目的是什么) |
|78 | [createElement() 和 cloneElement() 方法有什么区别?](#createelement-和-cloneelement-方法有什么区别) |
|79 | [推荐的组件命名方法是什么?](#推荐的组件命名方法是什么) |
|80 | [在组件类中方法的推荐顺序是什么?](#在组件类中方法的推荐顺序是什么) |
|81 | [什么是 switching 组件?](#什么是-switching-组件) |
|82 | [为什么我们需要将函数传递给 setState() 方法?](#为什么我们需要将函数传递给-setstate-方法) |
|83 | [在 React 中什么是严格模式?](#在-react-中什么是严格模式) |
|84 | [React Mixins 是什么?](#react-mixins-是什么) |
|85 | [为什么 `isMounted()` 是一个反模式，而正确的解决方案是什么?](#为什么-ismounted-是一个反模式而正确的解决方案是什么) |
|86 | [React 中支持哪些指针事件?](#react-中支持哪些指针事件) |
|87 | [为什么组件名称应该以大写字母开头?](#为什么组件名称应该以大写字母开头) |
|88 | [在 React v16 中是否支持自定义 DOM 属性?](#在-react-v16-中是否支持自定义-dom-属性) |
|89 | [constructor 和 getInitialState 有什么区别?](#constructor-和-getinitialstate-有什么区别) |
|90 | [是否可以在不调用 setState 方法的情况下，强制组件重新渲染?](#是否可以在不调用-setstate-方法的情况下强制组件重新渲染) |
|91 | [在使用 ES6 类的 React 中 `super()` 和 `super(props)` 有什么区别?](#在使用-es6-类的-react-中-super-和-superprops-有什么区别) |
|92 | [在 JSX 中如何进行循环?](#在-jsx-中如何进行循环) |
|93 | [如何在 attribute 引号中访问 props 属性?](#如何在-attribute-引号中访问-props-属性) |
|94 | [什么是 React proptype 数组?](#什么是-react-proptype-数组) |
|95 | [如何有条件地应用样式类?](#如何有条件地应用样式类) |
|96 | [React 和 ReactDOM 之间有什么区别?](#react-和-reactdom-之间有什么区别) |
|97 | [为什么 ReactDOM 从 React 分离出来?](#为什么-reactdom-从-react-分离出来) |
|98 | [如何使用 React label 元素?](#如何使用-react-label-元素) |
|99 | [如何合并多个内联的样式对象?](#如何合并多个内联的样式对象) |
|100 | [如何在调整浏览器大小时重新渲染视图?](#如何在调整浏览器大小时重新渲染视图) |
|101 | [`setState()` 和 `replaceState()` 方法之间有什么区别?](#setstate-和-replacestate-方法之间有什么区别) |
|102 | [如何监听状态变化?](#如何监听状态变化) |
|103 | [在 React 状态中删除数组元素的推荐方法是什么?](#在-react-状态中删除数组元素的推荐方法是什么) |
|104 | [在 React 中是否可以不在页面上渲染 HTML 内容?](#在-react-中是否可以不在页面上渲染-html-内容) |
|105 | [如何用 React 漂亮地显示 JSON?](#如何用-react-漂亮地显示-json) |
|106 | [为什么你不能更新 React 中的 props?](#为什么你不能更新-react-中的-props) |
|107 | [如何在页面加载时聚焦一个输入元素?](#如何在页面加载时聚焦一个输入元素) |
|108 | [更新状态中的对象有哪些可能的方法?](#更新状态中的对象有哪些可能的方法) |
|109 | [为什么函数比对象更适合于 `setState()`?](#为什么函数比对象更适合于-setstate) |
|110 | [我们如何在浏览器中找到当前正在运行的 React 版本?](#我们如何在浏览器中找到当前正在运行的-react-版本) |
|111 | [在 `create-react-app` 项目中导入 polyfills 的方法有哪些?](#在-create-react-app-项目中导入-polyfills-的方法有哪些) |
|112 | [如何在 create-react-app 中使用 https 而不是 http?](#如何在-create-react-app-中使用-https-而不是-http) |
|113 | [如何避免在 create-react-app 中使用相对路径导入?](#如何避免在-create-react-app-中使用相对路径导入) |
|114 | [如何为 React Router 添加 Google Analytics?](#如何为-react-router-添加-google-analytics) |
|115 | [如何每秒更新一个组件?](#如何每秒更新一个组件) |
|116 | [如何将 vendor prefixes 应用于 React 中的内联样式?](#如何将-vendor-prefixes-应用于-react-中的内联样式) |
|117 | [如何使用 React 和 ES6 导入和导出组件?](#如何使用-react-和-es6-导入和导出组件) |
|118 | [为什么 React 组件名称必须以大写字母开头?](#为什么-react-组件名称必须以大写字母开头) |
|119 | [为什么组件的构造函数只被调用一次?](#为什么组件的构造函数只被调用一次) |
|120 | [在 React 中如何定义常量?](#在-react-中如何定义常量) |
|121 | [在 React 中如何以编程方式触发点击事件?](#在-react-中如何以编程方式触发点击事件) |
|122 | [在 React 中是否可以使用 async/await?](#在-react-中是否可以使用-async/await) |
|123 | [React 项目常见的文件结构是什么?](#react-项目常见的文件结构是什么) |
|124 | [最流行的动画软件包是什么?](#最流行的动画软件包是什么) |
|125 | [模块化样式文件有什么好处?](#模块化样式文件有什么好处) |
|126 | [什么是 React 流行的特定 linters?](#什么是-react-流行的特定-linters) |
|127 | [如何发起 AJAX 调用以及应该在哪些组件生命周期方法中进行 AJAX 调用?](#如何发起-ajax-调用以及应该在哪些组件生命周期方法中进行-ajax-调用) |
|128 | [什么是渲染属性?](#什么是渲染属性) |
| | [React Router](#react-router) |
|129 | [什么是 React Router?](#什么是-react-router) |
|130 | [React Router 与 history 库的区别?](#react-router-与-history-库的区别) |
|131 | [在 React Router v4 中的`<Router>`组件是什么?](#在-react-router-v4-中的router组件是什么) |
|132 | [`history` 中的 `push()` 和 `replace()` 方法的目的是什么?](#history-中的-push-和-replace-方法的目的是什么) |
|133 | [如何使用在 React Router v4 中以编程的方式进行导航?](#如何使用在-react-router-v4-中以编程的方式进行导航) |
|134 | [如何在 React Router v4 中获取查询字符串参数?](#如何在-react-router-v4-中获取查询字符串参数) |
|135 | [为什么你会得到 "Router may have only one child element" 警告?](#为什么你会得到-"router-may-have-only-one-child-element"-警告) |
|136 | [如何在 React Router v4 中将 params 传递给 `history.push` 方法?](#如何在-react-router-v4-中将-params-传递给-history.push-方法) |
|137 | [如何实现默认页面或 404 页面?](#如何实现默认页面或-404-页面) |
|138 | [如何在 React Router v4 上获取历史对象?](#如何在-react-router-v4-上获取历史对象) |
|139 | [登录后如何执行自动重定向?](#登录后如何执行自动重定向) |
| | [React Internationalization](#react-internationalization) |
|140 | [什么是 React Intl?](#什么是-react-intl) |
|141 | [React Intl 的主要特性是什么?](#react-intl-的主要特性是什么) |
|142 | [在 React Intl 中有哪两种格式化方式?](#在-react-intl-中有哪两种格式化方式) |
|143 | [在 React Intl 中如何使用`<FormattedMessage>`作为占位符使用?](#在-react-intl-中如何使用formattedmessage作为占位符使用) |
|144 | [如何使用 React Intl 访问当前语言环境?](#如何使用-react-intl-访问当前语言环境) |
|145 | [如何使用 React Intl 格式化日期?](#如何使用-react-intl-格式化日期) |
| | [React Testing](#react-testing) |
|146 | [在 React 测试中什么是浅层渲染（Shallow Renderer）?](#在-react-测试中什么是浅层渲染shallow-renderer) |
|147 | [在 React 中 `TestRenderer` 包是什么?](#在-react-中-testrenderer-包是什么) |
|148 | [ReactTestUtils 包的目的是什么?](#reacttestutils-包的目的是什么) |
|149 | [什么是 Jest?](#什么是-jest) |
|150 | [Jest 对比 Jasmine 有什么优势?](#jest-对比-jasmine-有什么优势) |
|151 | [举一个简单的 Jest 测试用例](#举一个简单的-jest-测试用例) |
| | [React Redux](#react-redux) |
|152 | [什么是 Flux?](#什么是-flux) |
|153 | [什么是 Redux?](#什么是-redux) |
|154 | [Redux 的核心原则是什么？?](#redux-的核心原则是什么) |
|155 | [与 Flux 相比，Redux 的缺点是什么?](#与-flux-相比redux-的缺点是什么) |
|156 | [`mapStateToProps()` 和 `mapDispatchToProps()` 之间有什么区别?](#mapstatetoprops-和-mapdispatchtoprops-之间有什么区别) |
|157 | [我可以在 reducer 中触发一个 Action 吗?](#我可以在-reducer-中触发一个-action-吗) |
|158 | [如何在组件外部访问 Redux 存储的对象?](#如何在组件外部访问-redux-存储的对象) |
|159 | [MVW 模式的缺点是什么?](#mvw-模式的缺点是什么) |
|160 | [Redux 和 RxJS 之间是否有任何相似之处?](#redux-和-rxjs-之间是否有任何相似之处) |
|161 | [如何在加载时触发 Action?](#如何在加载时触发-action) |
|162 | [在 React 中如何使用 Redux 的 `connect()` ?](#在-react-中如何使用-redux-的-connect-) |
|163 | [如何在 Redux 中重置状态?](#如何在-redux-中重置状态) |
|164 | [Redux 中连接装饰器的 `at` 符号的目的是什么?](#redux-中连接装饰器的-at-符号的目的是什么) |
|165 | [React 上下文和 React Redux 之间有什么区别?](#react-上下文和-react-redux-之间有什么区别) |
|166 | [为什么 Redux 状态函数称为 reducers ?](#为什么-redux-状态函数称为-reducers-) |
|167 | [如何在 Redux 中发起 AJAX 请求?](#如何在-redux-中发起-ajax-请求) |
|168 | [我应该在 Redux Store 中保留所有组件的状态吗?](#我应该在-redux-store-中保留所有组件的状态吗) |
|169 | [访问 Redux Store 的正确方法是什么?](#访问-redux-store-的正确方法是什么) |
|170 | [React Redux 中展示组件和容器组件之间的区别是什么?](#react-redux-中展示组件和容器组件之间的区别是什么) |
|171 | [Redux 中常量的用途是什么?](#redux-中常量的用途是什么) |
|172 | [编写 `mapDispatchToProps()` 有哪些不同的方法?](#编写-mapdispatchtoprops-有哪些不同的方法) |
|173 | [在 `mapStateToProps()` 和 `mapDispatchToProps()` 中使用 `ownProps` 参数有什么用?](#在-mapstatetoprops-和-mapdispatchtoprops-中使用-ownprops-参数有什么用) |
|174 | [如何构建 Redux 项目目录?](#如何构建-redux-项目目录) |
|175 | [什么是 redux-saga?](#什么是-redux-saga) |
|176 | [redux-saga 的模型概念是什么?](#redux-saga-的模型概念是什么) |
|177 | [在 redux-saga 中 `call()` 和 `put()` 之间有什么区别?](#在-redux-saga-中-call-和-put-之间有什么区别) |
|178 | [什么是 Redux Thunk?](#什么是-redux-thunk) |
|179 | [`redux-saga` 和 `redux-thunk` 之间有什么区别?](#redux-saga-和-redux-thunk-之间有什么区别) |
|180 | [什么是 Redux DevTools?](#什么是-redux-devtools) |
|181 | [Redux DevTools 的功能有哪些?](#redux-devtools-的功能有哪些) |
|182 | [什么是 Redux 选择器以及使用它们的原因?](#什么是-redux-选择器以及使用它们的原因) |
|183 | [什么是 Redux Form?](#什么是-redux-form) |
|184 | [Redux Form 的主要功能有哪些?](#redux-form-的主要功能有哪些) |
|185 | [如何向 Redux 添加多个中间件?](#如何向-redux-添加多个中间件) |
|186 | [如何在 Redux 中设置初始状态?](#如何在-redux-中设置初始状态) |
|187 | [Relay 与 Redux 有何不同?](#relay-与-redux-有何不同) |
| | [React Native](#react-native) |
|188 | [React Native 和 React 有什么区别?](#react-native-和-react-有什么区别) |
|189 | [如何测试 React Native 应用程序?](#如何测试-react-native-应用程序) |
|190 | [如何在 React Native 查看日志?](#如何在-react-native-查看日志) |
|191 | [怎么调试 React Native 应用?](#怎么调试-react-native-应用) |
| | [React supported libraries & Integration](#react-supported-libraries-&-integration) |
|192 | [什么是 Reselect 以及它是如何工作的?](#什么是-reselect-以及它是如何工作的) |
|193 | [什么是 Flow?](#什么是-flow) |
|194 | [Flow 和 PropTypes 有什么区别?](#flow-和-proptypes-有什么区别) |
|195 | [在 React 中如何使用 Font Awesome 图标?](#在-react-中如何使用-font-awesome-图标) |
|196 | [什么 是 React 开发者工具?](#什么-是-react-开发者工具) |
|197 | [在 Chrome 中为什么 DevTools 没有加载本地文件?](#在-chrome-中为什么-devtools-没有加载本地文件) |
|198 | [如何在 React 中使用 Polymer?](#如何在-react-中使用-polymer) |
|199 | [与 Vue.js 相比，React 有哪些优势?](#与-vue.js-相比react-有哪些优势) |
|200 | [React 和 Angular 有什么区别?](#react-和-angular-有什么区别) |
|201 | [为什么 React 选项卡不会显示在 DevTools 中?](#为什么-react-选项卡不会显示在-devtools-中) |
|202 | [什么是 Styled Components?](#什么是-styled-components) |
|203 | [举一个 Styled Components 的例子?](#举一个-styled-components-的例子) |
|204 | [什么是 Relay?](#什么是-relay) |
|205 | [如何在 `create-react-app` 中使用 TypeScript?](#如何在-create-react-app-中使用-typescript) |
| | [Miscellaneous](#miscellaneous) |
|206 | [Reselect 库的主要功能有哪些?](#reselect-库的主要功能有哪些) |
|207 | [举一个 Reselect 用法的例子?](#举一个-reselect-用法的例子) |
|208 | [Redux 中的 Action 是什么?](#redux-中的-action-是什么) |
|209 | [在 React 中 statics 对象是否能与 ES6 类一起使用?](#在-react-中-statics-对象是否能与-es6-类一起使用) |
|210 | [Redux 只能与 React 一起使用么?](#redux-只能与-react-一起使用么) |
|211 | [您是否需要使用特定的构建工具来使用 Redux ?](#您是否需要使用特定的构建工具来使用-redux-) |
|212 | [Redux Form 的 `initialValues` 如何从状态更新?](#redux-form-的-initialvalues-如何从状态更新) |
|213 | [React 是如何为一个属性声明不同的类型?](#react-是如何为一个属性声明不同的类型) |
|214 | [我可以导入一个 SVG 文件作为 React 组件么?](#我可以导入一个-svg-文件作为-react-组件么) |
|215 | [为什么不建议使用内联引用回调或函数?](#为什么不建议使用内联引用回调或函数) |
|216 | [在 React 中什么是渲染劫持?](#在-react-中什么是渲染劫持) |
|217 | [什么是 HOC 工厂实现?](#什么是-hoc-工厂实现) |
|218 | [如何传递数字给 React 组件?](#如何传递数字给-react-组件) |
|219 | [我需要将所有状态保存到 Redux 中吗？我应该使用 react 的内部状态吗?](#我需要将所有状态保存到-redux-中吗我应该使用-react-的内部状态吗) |
|220 | [在 React 中 registerServiceWorker 的用途是什么?](#在-react-中-registerserviceworker-的用途是什么) |
|221 | [React memo 函数是什么?](#react-memo-函数是什么) |
|222 | [React lazy 函数是什么?](#react-lazy-函数是什么) |
|223 | [如何使用 setState 防止不必要的更新?](#如何使用-setstate-防止不必要的更新) |
|224 | [如何在 React 16 版本中渲染数组、字符串和数值? ](#如何在-react-16-版本中渲染数组、字符串和数值-) |
|225 | [如何在 React 类中使用类字段声明语法?](#如何在-react-类中使用类字段声明语法) |
|226 | [什么是 hooks?](#什么是-hooks) |
|227 | [Hooks 需要遵循什么规则?](#hooks-需要遵循什么规则) |
|228 | [如何确保钩子遵循正确的使用规则?](#如何确保钩子遵循正确的使用规则) |
|229 | [Flux 和 Redux 之间有什么区别?](#flux-和-redux-之间有什么区别) |
|230 | [React Router V4 有什么好处?](#react-router-v4-有什么好处) |
|231 | [您能描述一下 componentDidCatch 生命周期方法签名吗?](#您能描述一下-componentdidcatch-生命周期方法签名吗) |
|232 | [在哪些情况下，错误边界不会捕获错误?](#在哪些情况下错误边界不会捕获错误) |
|233 | [为什么事件处理器不需要错误边界?](#为什么事件处理器不需要错误边界) |
|234 | [try catch 与错误边界有什么区别?](#try-catch-与错误边界有什么区别) |
|235 | [React 16 中未捕获的错误的行为是什么?](#react-16-中未捕获的错误的行为是什么) |
|236 | [放置错误边界的正确位置是什么?](#放置错误边界的正确位置是什么) |
|237 | [从错误边界跟踪组件堆栈有什么好处?](#从错误边界跟踪组件堆栈有什么好处) |
|238 | [在定义类组件时，什么是必须的方法?](#在定义类组件时什么是必须的方法) |
|239 | [render 方法可能返回的类型是什么?](#render-方法可能返回的类型是什么) |
|240 | [构造函数的主要目的是什么?](#构造函数的主要目的是什么) |
|241 | [是否必须为 React 组件定义构造函数?](#是否必须为-react-组件定义构造函数) |
|242 | [什么是默认属性?](#什么是默认属性) |
|243 | [为什么不能在 componentWillUnmount 中调用 setState() 方法?](#为什么不能在-componentwillunmount-中调用-setstate-方法) |
|244 | [getDerivedStateFromError 的目的是什么?](#getderivedstatefromerror-的目的是什么) |
|245 | [当组件重新渲染时顺序执行的方法有哪些?](#当组件重新渲染时顺序执行的方法有哪些) |
|246 | [错误处理期间调用哪些方法?](#错误处理期间调用哪些方法) |
|247 | [displayName 类属性的用途是什么?](#displayname-类属性的用途是什么) |
|248 | [支持 React 应用程序的浏览器有哪一些?](#支持-react-应用程序的浏览器有哪一些) |
|249 | [unmountComponentAtNode 方法的目的是什么?](#unmountcomponentatnode-方法的目的是什么) |
|250 | [什么是代码拆分?](#什么是代码拆分) |
|251 | [严格模式有什么好处?](#严格模式有什么好处) |
|252 | [什么是 Keyed Fragments ?](#什么是-keyed-fragments-) |
|253 | [React 支持所有的 HTML 属性么?](#react-支持所有的-html-属性么) |
|254 | [HOC 有哪些限制?](#hoc-有哪些限制) |
|255 | [如何在 DevTools 中调试 forwardRefs?](#如何在-devtools-中调试-forwardrefs) |
|256 | [什么时候组件的 props 属性默认为 true?](#什么时候组件的-props-属性默认为-true) |
|257 | [什么是 NextJS 及其主要特征?](#什么是-nextjs-及其主要特征) |
|258 | [如何将事件处理程序传递给组件?](#如何将事件处理程序传递给组件) |
|259 | [在渲染方法中使用箭头函数好么?](#在渲染方法中使用箭头函数好么) |
|260 | [如何防止函数被多次调用?](#如何防止函数被多次调用) |
|261 | [JSX 如何防止注入攻击?](#jsx-如何防止注入攻击) |
|262 | [如何更新已渲染的元素?](#如何更新已渲染的元素) |
|263 | [你怎么说 props 是只读的?](#你怎么说-props-是只读的) |
|264 | [你认为状态更新是如何合并的?](#你认为状态更新是如何合并的) |
|265 | [如何将参数传递给事件处理程序?](#如何将参数传递给事件处理程序) |
|266 | [如何防止组件渲染?](#如何防止组件渲染) |
|267 | [安全地使用索引作为键的条件是什么?](#安全地使用索引作为键的条件是什么) |
|268 | [keys 是否需要全局唯一?](#keys-是否需要全局唯一) |
|269 | [用于表单处理的流行选择是什么?](#用于表单处理的流行选择是什么) |
|270 | [formik 相对于其他 redux 表单库有什么优势?](#formik-相对于其他-redux-表单库有什么优势) |
|271 | [为什么不需要使用继承?](#为什么不需要使用继承) |
|272 | [我可以在 React 应用程序中可以使用 web components 么?](#我可以在-react-应用程序中可以使用-web-components-么) |
|273 | [什么是动态导入?](#什么是动态导入) |
|274 | [什么是 loadable 组件?](#什么是-loadable-组件) |
|275 | [什么是 suspense 组件?](#什么是-suspense-组件) |
|276 | [什么是基于路由的代码拆分?](#什么是基于路由的代码拆分) |
|277 | [举例说明如何使用 context?](#举例说明如何使用-context) |
|278 | [在 context 中默认值的目的是什么?](#在-context-中默认值的目的是什么) |
|279 | [你是怎么使用 contextType?](#你是怎么使用-contexttype) |
|280 | [什么是 consumer?](#什么是-consumer) |
|281 | [在使用 context 时，如何解决性能方面的问题?](#在使用-context-时如何解决性能方面的问题) |
|282 | [在 HOCs 中 forward ref 的目的是什么?](#在-hocs-中-forward-ref-的目的是什么) |
|283 | [ref 参数对于所有函数或类组件是否可用?](#ref-参数对于所有函数或类组件是否可用) |
|284 | [在组件库中当使用 forward refs 时，你需要额外的注意?](#在组件库中当使用-forward-refs-时你需要额外的注意) |
|285 | [如何在没有 ES6 的情况下创建 React 类组件](#如何在没有-es6-的情况下创建-react-类组件) |
|286 | [是否可以在没有 JSX 的情况下使用 React?](#是否可以在没有-jsx-的情况下使用-react) |
|287 | [什么是差异算法?](#什么是差异算法) |
|288 | [差异算法涵盖了哪些规则?](#差异算法涵盖了哪些规则) |
|289 | [你什么时候需要使用 refs?](#你什么时候需要使用-refs) |
|290 | [对于渲染属性来说是否必须将 prop 属性命名为 render?](#对于渲染属性来说是否必须将-prop-属性命名为-render) |
|291 | [在 Pure Component 中使用渲染属性会有什么问题?](#在-pure-component-中使用渲染属性会有什么问题) |
|292 | [如何使用渲染属性创建 HOC?](#如何使用渲染属性创建-hoc) |
|293 | [什么是 windowing 技术?](#什么是-windowing-技术) |
|294 | [你如何在 JSX 中打印 falsy 值?](#你如何在-jsx-中打印-falsy-值) |
|295 | [portals 的典型使用场景是什么?](#portals-的典型使用场景是什么) |
|296 | [如何设置非受控组件的默认值?](#如何设置非受控组件的默认值) |
|297 | [你最喜欢的 React 技术栈是什么?](#你最喜欢的-react-技术栈是什么) |
|298 | [Real DOM 和 Virtual DOM 有什么区别?](#real-dom-和-virtual-dom-有什么区别) |
<!-- /TOC -->

## Core React

1. ### 什么是 React?

    [React](https://reactjs.org/) 是一个**开源前端 JavaScript 库**，用于构建用户界面，尤其是单页应用程序。它用于处理网页和移动应用程序的视图层。React 是由 Facebook 的软件工程师 Jordan Walke 创建的。在 2011 年 React 应用首次被部署到 Facebook 的信息流中，之后于 2012 年被应用到 Instagram 上。


    **[⬆ 返回顶部](#目录)**

2. ### React 的主要特点是什么?

    React 的主要特性有：

    * 考虑到真实的 DOM 操作成本很高，它使用 VirtualDOM 而不是真实的 DOM。
    * 支持服务端渲染。
    * 遵循单向数据流或数据绑定。
    * 使用可复用/可组合的 UI 组件开发视图。

    **[⬆ 返回顶部](#目录)**

3. ### 什么是 JSX?

    JSX 是 ECMAScript 一个类似 XML 的语法扩展。基本上，它只是为 `React.createElement()` 函数提供语法糖，从而让在我们在 JavaScript 中，使用类 HTML 模板的语法，进行页面描述。

    **[⬆ 返回顶部](#目录)**

4. ### 元素和组件有什么区别?

    一个 *Element* 是一个简单的对象，它描述了你希望在屏幕上以 DOM 节点或其他组件的形式呈现的内容。*Elements* 在它们的属性中可以包含其他 *Elements*。创建一个 React 元素是很轻量的。一旦元素被创建后，它将不会被修改。组件可以用几种不同的声明方式。它可以是一个带有render方法的类。或者，在简单(你可以认为是没有状态)的情况下，可以将其定义为函数。在任何一种情况下，它都将props作为输入，并返回一个元素树作为输出。当一个组件接收一些props作为输入时，这是因为一个特定的父组件返回了一个元素及其类型和这些props。

    **[⬆ 返回顶部](#目录)**

5. ### 如何在 React 中创建组件?

    有两种可行的方法来创建一个组件：

    1. **Function Components:** （函数组件）这是创建组件最简单的方式。这些是纯 JavaScript 函数，接受 props 对象作为第一个参数并返回 React 元素。
    2. **Class Components:** （类组件）你还可以使用 ES6 类来定义组件。

    **[⬆ 返回顶部](#目录)**

6. ### 何时使用类组件和函数组件?

    如果组件需要使用**状态或生命周期方法**，那么使用类组件，否则使用函数组件。

    **[⬆ 返回顶部](#目录)**

7. ### 什么是 Pure Components?

    `React.PureComponent` 与 `React.Component` 完全相同，只是它为你处理了 `shouldComponentUpdate()` 方法。当属性或状态发生变化时，PureComponent 将对属性和状态进行**浅比较**。另一方面，一般的组件不会将当前的属性和状态与新的属性和状态进行比较。因此，在默认情况下，每当调用 `shouldComponentUpdate` 时，默认返回 true，所以组件都将重新渲染。

    **[⬆ 返回顶部](#目录)**

8. ### React 的状态是什么?

    组件的状态是一个对象，它包含某些信息，这些信息可能在组件的生命周期中发生更改。我们应该尽量使状态尽可能简单，并尽量减少有状态组件的数量。

    ![Sample Pic][state]

    状态（State）与属性（Props）类似，但它是私有的，完全由组件控制。也就是说，除了它所属的组件外，任何组件都无法访问它。

    **[⬆ 返回顶部](#目录)**

9. ### React 中的 props 是什么?

    Props 是组件的输入。它们是单个值或包含一组值的对象，这些值在创建时使用类似于 HTML 标记属性的命名约定传递给组件。它们是从父组件传递到子组件的数据。

    Props 的主要目的是提供以下组件功能：

    1. 将自定义数据传递到组件。
    2. 触发状态更改。
    3. 在组件的 `render()` 方法中通过 `this.props.reactProp` 使用。

    **[⬆ 返回顶部](#目录)**

10. ### 状态和属性有什么区别?

    state 和 props 都是普通的 JavaScript 对象。虽然它们都保存着影响渲染输出的信息，但它们在组件方面的功能不同。Props 以类似于函数参数的方式传递给组件，而状态则类似于在函数内声明变量并对它进行管理。

    States vs Props

    | Conditions           | States | Props |
    | -------------------- | ------ | ----- |
    | 可从父组件接收初始值 | 是     | 是    |
    | 可在父组件中改变其值 | 否     | 是    |
    | 在组件内设置默认值   | 是     | 是    |
    | 在组件内可改变       | 是     | 否    |
    | 可作为子组件的初始值 | 是     | 是    |

    **[⬆ 返回顶部](#目录)**

11. ### 我们为什么不能直接更新状态?

    如果你尝试直接改变状态，那么组件将不会重新渲染。
    正确方法应该是使用 `setState()` 方法。它调度组件状态对象的更新。当状态更改时，组件通将会重新渲染。

    **注意：** 你可以在 *constructor* 中或使用最新的 JavaScript 类属性声明语法直接设置状态对象。

    **[⬆ 返回顶部](#目录)**

12. ### 回调函数作为 `setState()` 参数的目的是什么?

    当 setState 完成和组件渲染后，回调函数将会被调用。由于 `setState()` 是异步的，回调函数用于任何后续的操作。

    **注意：** 建议使用生命周期方法而不是此回调函数。

    **[⬆ 返回顶部](#目录)**

13. ### HTML 和 React 事件处理有什么区别?

    1. 在 HTML 中事件名必须小写：

    而在 React 中它遵循 *camelCase* (驼峰) 惯例

    2. 在 HTML 中你可以返回 `false` 以阻止默认的行为：
    而在 React 中你必须地明确地调用 `preventDefault()` 

    **[⬆ 返回顶部](#目录)**

14. ### 如何在 JSX 回调中绑定方法或事件处理程序?

    实现这一点有三种可能的方法：

    1.	**Binding in Constructor:**（绑定在构造函数） 在 JavaScript 类中，方法默认不被绑定。这也适用于定义为类方法的 React 事件处理程序。通常我们在构造函数中绑定它们。

    2. **Public class fields syntax:** 如果你不喜欢 bind 方案，则可以使用 *public class fields syntax* 正确绑定回调。

    3. **Arrow functions in callbacks:**（箭头函数） 你可以在回调函数中直接使用 *arrow functions*（箭头函数）。

    **注意：** 如果回调函数作为属性传给子组件，那么这些组件可能触发一个额外的重新渲染。在这些情况下，考虑到性能，最好使用 `.bind()` 或 *public class fields syntax* 方案。

    **[⬆ 返回顶部](#目录)**

15. ### 如何将参数传递给事件处理程序或回调函数?

    你可以使用箭头函数来包装事件处理器并传递参数：

    ```jsx 
    <button onClick={() => this.handleClick(id)} />
    ```

    这相当于调用 `.bind`:

    ```jsx 
    <button onClick={this.handleClick.bind(this, id)} />
    ```

    **[⬆ 返回顶部](#目录)**

16. ### React 中的合成事件是什么?

    `SyntheticEvent` 是对浏览器原生事件的跨浏览器包装。它的 API 与浏览器的原生事件相同，包括 `stopPropagation()` 和 `preventDefault()`，除了事件在所有浏览器中的工作方式相同。

    **[⬆ 返回顶部](#目录)**

17. ### 什么是内联条件表达式?

    在 JS 中你可以使用 if 语句或三元表达式，来实现条件判断。除了这些方法之外，你还可以在 JSX 中嵌入任何表达式，方法是将它们用大括号括起来，然后再加上 JS 逻辑运算符 `&&`。
    **[⬆ 返回顶部](#目录)**

19. ### refs 有什么用?

    *ref* 用于返回对元素的引用。

20. ### 如何创建 refs?

    1. *Refs* 是使用 `React.createRef()` 方法创建的，并通过 `ref` 属性添加到 React 元素上。为了在整个组件中使用*refs*，只需将 *ref* 分配给构造函数中的实例属性。

    **[⬆ 返回顶部](#目录)**

21. ### 什么是 forward refs?

    *Ref forwarding* 是一个特性，它允许一些组件获取接收到 *ref* 对象并将它进一步传递给子组件。      

    **[⬆ 返回顶部](#目录)**

22. ### callback refs 和 findDOMNode() 哪一个是首选选项?

    最好是使用 *callback refs* 而不是 `findDOMNode()` API。因为 `findDOMNode()` 阻碍了将来对 React 的某些改进。

    **[⬆ 返回顶部](#目录)**

23. ### 为什么 String Refs 被弃用?

    如果你以前使用过 React，你可能会熟悉旧的 API，其中的 `ref` 属性是字符串，如 `ref={'textInput'}`，并且 DOM 节点的访问方式为`this.refs.textInput`。我们建议不要这样做，因为字符串引用有以下问题，并且被认为是遗留问题。字符串 refs 在 React v16 版本中被移除。

    1. 它们强制 React 跟踪当前执行的组件。这是有问题的，因为它使 React 模块有状态，这会导致在 bundle 中复制 React 模块时会导致奇怪的错误。
    2. 它们是不可组合的 - 如果一个库把一个 ref 传给子元素，则用户无法对其设置另一个引用。
    3. 它们不能与静态分析工具一起使用，如 Flow。Flow 无法猜测出 `this.refs` 上的字符串引用的作用及其类型。Callback refs 对静态分析更友好。
    4. 使用 "render callback" 模式（比如： <DataGrid renderRow={this.renderRow} />），它无法像大多数人预期的那样工作。

    **[⬆ 返回顶部](#目录)**

24. ### 什么是 Virtual DOM?

    *Virtual DOM* (VDOM) 是 *Real DOM* 的内存表示形式。UI 的展示形式被保存在内存中并与真实的 DOM 同步。这是在调用的渲染函数和在屏幕上显示元素之间发生的一个步骤。整个过程被称为 *reconciliation*（调解）。

    Real DOM vs Virtual DOM

    |           Real DOM           |       Virtual DOM        |
    | :--------------------------: | :----------------------: |
    |           更新较慢           |         更新较快         |
    |      可以直接更新 HTML       |    无法直接更新 HTML     |
    | 如果元素更新，则创建新的 DOM | 如果元素更新，则更新 JSX |
    |       DOM 操作非常昂贵       |     DOM 操作非常简单     |
    |        较多的内存浪费        |       没有内存浪费       |

    **[⬆ 返回顶部](#目录)**

25. ### Virtual DOM 如何工作?

    *Virtual DOM* 分为三个简单的步骤。

    1. 每当任何底层数据发生更改时，整个 UI 都将以 Virtual DOM 的形式重新渲染。
        ![vdom](images/vdom1.png)

    2. 然后计算先前 Virtual DOM 对象和新的 Virtual DOM 对象之间的差异。
        ![vdom2](images/vdom2.png)

    3. 一旦计算完成，真实的 DOM 将只更新实际更改的内容。
        ![vdom3](images/vdom3.png)

    **[⬆ 返回顶部](#目录)**

27. ### 什么是 React Fiber?

    Fiber 是 React v16 中新的 *reconciliation* 引擎，或核心算法的重新实现。React Fiber 的目标是提高对动画，布局，手势，暂停，中止或者重用任务的能力及为不同类型的更新分配优先级，及新的并发原语等领域的适用性。

    **[⬆ 返回顶部](#目录)**

28. ### React Fiber 的主要目标是什么?

    *React Fiber* 的目标是提高其在动画、布局和手势等领域的适用性。它的主要特性是 **incremental rendering**（增量渲染）: 将渲染任务拆分为小的任务块并将任务分配到多个帧上的能力。

    **[⬆ 返回顶部](#目录)**

29. ### 什么是受控组件?

    在随后的用户输入中，能够控制表单中输入元素的组件被称为受控组件，即每个状态更改都有一个相关联的处理程序。

    **[⬆ 返回顶部](#目录)**

30. ### 什么是非受控组件?

    非受控组件是在内部存储其自身状态的组件，当需要时，可以使用 ref 查询 DOM 并查找其当前值。这有点像传统的 HTML。

    **[⬆ 返回顶部](#目录)**

31. ### createElement 和 cloneElement 有什么区别?

    JSX 元素将被转换为 `React.createElement()` 函数来创建 React 元素，这些对象将用于表示 UI 对象。而 `cloneElement` 用于克隆元素并传递新的属性。

    **[⬆ 返回顶部](#目录)**

32. ### 在 React 中的提升状态是什么?

    当多个组件需要共享相同的更改数据时，建议将共享状态提升到最接近的共同祖先。这意味着，如果两个子组件共享来自其父组件的相同数据，则将状态移动到父组件，而不是在两个子组件中维护局部状态。

    **[⬆ 返回顶部](#目录)**

33. ### 组件生命周期的不同阶段是什么?

    组件生命周期有三个不同的生命周期阶段：

    1. **Mounting:** 组件已准备好挂载到浏览器的 DOM 中. 此阶段包含来自 `constructor()`, `getDerivedStateFromProps()`, `render()`, 和 `componentDidMount()` 生命周期方法中的初始化过程。

    2. **Updating:** 在此阶段，组件以两种方式更新，发送新的属性并使用 `setState()` 或 `forceUpdate()` 方法更新状态. 此阶段包含 `getDerivedStateFromProps()`, `shouldComponentUpdate()`, `render()`, `getSnapshotBeforeUpdate()` 和 `componentDidUpdate()` 生命周期方法。

    3. **Unmounting:** 在这个最后阶段，不需要组件，它将从浏览器 DOM 中卸载。这个阶段包含 `componentWillUnmount()` 生命周期方法。

    值得一提的是，在将更改应用到 DOM 时，React 内部也有阶段概念。它们按如下方式分隔开：

    1. **Render** 组件将会进行无副作用渲染。这适用于纯组件（Pure Component），在此阶段，React 可以暂停，中止或重新渲染。

    2. **Pre-commit** 在组件实际将更改应用于 DOM 之前，有一个时刻允许 React 通过`getSnapshotBeforeUpdate()`捕获一些 DOM 信息（例如滚动位置）。

    3. **Commit** React 操作 DOM 并分别执行最后的生命周期： `componentDidMount()` 在 DOM 渲染完成后调用, `componentDidUpdate()` 在组件更新时调用,  `componentWillUnmount()` 在组件卸载时调用。
    React 16.3+ 阶段 (也可以看[交互式版本](http://projects.wojtekmaj.pl/react-lifecycle-methods-diagram/))

    ![phases 16.3+](images/phases16.3.jpg)

    React 16.3 之前

    ![phases 16.2](images/phases.png)

    **[⬆ 返回顶部](#目录)**


34. ### React 生命周期方法有哪些?

    React 16.3+

    - **getDerivedStateFromProps:** 在调用`render()`之前调用，并在 *每次* 渲染时调用。 需要使用派生状态的情况是很罕见得。值得阅读 [如果你需要派生状态](https://reactjs.org/blog/2018/06/07/you-probably-dont-need-derived-state.html).
    - **componentDidMount:** 首次渲染后调用，所有得 Ajax 请求、DOM 或状态更新、设置事件监听器都应该在此处发生。
    - **shouldComponentUpdate:** 确定组件是否应该更新。 默认情况下，它返回`true`。 如果你确定在更新状态或属性后不需要渲染组件，则可以返回`false`值。 它是一个提高性能的好地方，因为它允许你在组件接收新属性时阻止重新渲染。
    - **getSnapshotBeforeUpdate:** 在最新的渲染输出提交给 DOM 前将会立即调用，这对于从 DOM 捕获信息（比如：滚动位置）很有用。
    - **componentDidUpdate:** 它主要用于更新 DOM 以响应 prop 或 state 更改。 如果`shouldComponentUpdate()`返回`false`，则不会触发。
    - **componentWillUnmount** 当一个组件被从 DOM 中移除时，该方法被调用，取消网络请求或者移除与该组件相关的事件监听程序等应该在这里进行。

    Before 16.3

    - **componentWillMount:** 在组件`render()`前执行，用于根组件中的应用程序级别配置。应该避免在该方法中引入任何的副作用或订阅。
    - **componentDidMount:** 首次渲染后调用，所有得 Ajax 请求、DOM 或状态更新、设置事件监听器都应该在此处发生。
    - **componentWillReceiveProps:** 在组件接收到新属性前调用，若你需要更新状态响应属性改变（例如，重置它），你可能需对比`this.props`和`nextProps`并在该方法中使用`this.setState()`处理状态改变。
    - **shouldComponentUpdate:** 确定组件是否应该更新。 默认情况下，它返回`true`。 如果你确定在更新状态或属性后不需要渲染组件，则可以返回`false`值。 它是一个提高性能的好地方，因为它允许你在组件接收新属性时阻止重新渲染。
    - **componentWillUpdate:** 当`shouldComponentUpdate`返回`true`后重新渲染组件之前执行，注意你不能在这调用`this.setState()`
    - **componentDidUpdate:** 它主要用于更新 DOM 以响应 prop 或 state 更改。 如果`shouldComponentUpdate()`返回`false`，则不会触发。
    - **componentWillUnmount:** 当一个组件被从 DOM 中移除时，该方法被调用，取消网络请求或者移除与该组件相关的事件监听程序等应该在这里进行。

    **[⬆ 返回顶部](#目录)**

35. ### 什么是高阶组件（HOC）?

    *高阶组件*(*HOC*) 就是一个函数，且该函数接受一个组件作为参数，并返回一个新的组件，它只是一种模式，这种模式是由`react`自身的组合性质必然产生的。

    我们将它们称为**纯组件**，因为它们可以接受任何动态提供的子组件，但它们不会修改或复制其输入组件中的任何行为。

    HOC 有很多用例：

    1. 代码复用，逻辑抽象化
    2. 渲染劫持
    3. 抽象化和操作状态（`state`）
    4. 操作属性（`props`）

    **[⬆ 返回顶部](#目录)**

36. ### 如何为高阶组件创建属性代理?

    你可以使用*属性代理*模式向输入组件增加或编辑属性（props）

    **[⬆ 返回顶部](#目录)**

37. ### 什么是上下文（Context）?

    *Context* 通过组件树提供了一个传递数据的方法，从而避免了在每一个层级手动的传递`props`。比如，需要在应用中许多组件需要访问登录用户信息、地区偏好、UI主题等。

    **[⬆ 返回顶部](#目录)**

38. ### children 属性是什么?

    *Children* 是一个属性（`this.props.chldren`），它允许你将组件作为数据传递给其他组件，就像你使用的任何其他组件一样。在组件的开始和结束标记之间放置的组件树将作为`children`属性传递给该组件。

    React API 中有许多方法中提供了这个不透明数据结构的方法，包括：`React.Children.map`、`React.Children.forEach`、`React.Children.count`、`React.Children.only`、`React.Children.toArray`。

    **[⬆ 返回顶部](#目录)**

40. ### 构造函数使用带 props 参数的目的是什么?

    在调用`super()`方法之前，子类构造函数不能使用`this`引用。这同样适用于ES6子类。将`props`参数传递给`super()`的主要原因是为了在子构造函数中访问`this.props`。

    **[⬆ 返回顶部](#目录)**

41. ### 什么是调解?

    当组件的`props`或`state`发生更改时，React 通过将新返回的元素与先前呈现的元素进行比较来确定是否需要实际的 DOM 更新。当它们不相等时，React 将更新 DOM 。此过程称为*reconciliation*。

    **[⬆ 返回顶部](#目录)**

42. ### 如何使用动态属性名设置 state ?

    如果你使用 ES6 或 Babel 转换器来转换你的 JSX 代码，那么你可以使用*计算属性名称*来完成此操作。

    **[⬆ 返回顶部](#目录)**

43. ### 每次组件渲染时调用函数的常见错误是什么?

    你需要确保在将函数作为参数传递时未调用该函数。

    **[⬆ 返回顶部](#目录)**

44. ### 为什么有组件名称要首字母大写?

    这是必要的，因为组件不是 DOM 元素，它们是构造函数。 此外，在 JSX 中，小写标记名称是指 HTML 元素，而不是组件。

    **[⬆ 返回顶部](#目录)**

45. ### 为什么 React 使用 `className` 而不是 `class` 属性?

    `class` 是 JavaScript 中的关键字，而 JSX 是 JavaScript 的扩展。这就是为什么 React 使用 `className` 而不是 `class` 的主要原因。传递一个字符串作为 `className` 属性。
    
    在实际项目中，我们经常使用[classnames](https://github.com/JedWatson/classnames)来方便我们操作`className`。

    **[⬆ 返回顶部](#目录)**

46. ### 什么是 Fragments ?

    它是 React 中的常见模式，用于组件返回多个元素。*Fragments*（文档碎片） 可以让你聚合一个子元素列表，而无需向 DOM 添加额外节点。

    **[⬆ 返回顶部](#目录)**

47. ### 为什么使用 Fragments 比使用容器 div 更好?

    1. 通过不创建额外的 DOM 节点，Fragments 更快并且使用更少的内存。这在非常大而深的节点树时很有好处。
    2. 一些 CSS 机制如*Flexbox*（弹性盒）和*CSS Grid*（网格布局）具有特殊的父子关系，如果在中间添加 div 将使得很难保持所需的结构。
    3. 在 DOM 审查器中不会那么的杂乱。

    **[⬆ 返回顶部](#目录)**

48. ### 在 React 中什么是 Portal ?

    *Portal* 提供了一种很好的将子节点渲染到父组件以外的 DOM 节点的方式。

    第一个参数是任何可渲染的 React 子节点，例如元素，字符串或片段。第二个参数是 DOM 元素。

    **[⬆ 返回顶部](#目录)**

49. ### 什么是无状态组件?

    如果行为独立于其状态，则它可以是无状态组件。你可以使用函数或类来创建无状态组件。但除非你需要在组件中使用生命周期钩子，否则你应该选择函数组件。无状态组件有很多好处： 它们易于编写，理解和测试，速度更快，而且你可以完全避免使用`this`关键字。

    **[⬆ 返回顶部](#目录)**

50. ### 什么是有状态组件?

    如果组件的行为依赖于组件的*state*，那么它可以被称为有状态组件。这些*有状态组件*总是*类组件*，并且具有在`constructor`中初始化的状态。

    **[⬆ 返回顶部](#目录)**

51. ### 在 React 中如何校验 props 属性?

    当应用程序以开发模式运行的时，React 将会自动检查我们在组件上设置的所有属性，以确保它们具有正确的类型。如果类型不正确，React 将在控制台中生成警告信息。由于性能影响，它在生产模式下被禁用。使用 `isRequired` 定义必填属性。

    预定义的 prop 类型：

    1. `PropTypes.number`
    2. `PropTypes.string`
    3. `PropTypes.array`
    4. `PropTypes.object`
    5. `PropTypes.func`
    6. `PropTypes.node`
    7. `PropTypes.element`
    8. `PropTypes.bool`
    9. `PropTypes.symbol`
    10. `PropTypes.any`

    **注意:** 在 React v15.5 中，*PropTypes* 从 `React.PropTypes` 被移动到 `prop-types` 库中。

    **[⬆ 返回顶部](#目录)**

52. ### React 的优点是什么?

    1. 使用 *Virtual DOM* 提高应用程序的性能。
    2. JSX 使代码易于读写。
    3. 它支持在客户端和服务端渲染。
    4. 易于与框架（Angular，Backbone）集成，因为它只是一个视图库。
    5. 使用 Jest 等工具轻松编写单元与集成测试。

    **[⬆ 返回顶部](#目录)**

53. ### React 的局限性是什么?

    1. React 只是一个视图库，而不是一个完整的框架。
    2. 对于 Web 开发初学者来说，有一个学习曲线。
    3. 将 React 集成到传统的 MVC 框架中需要一些额外的配置。
    4. 代码复杂性随着内联模板和 JSX 的增加而增加。
    5. 如果有太多的小组件可能增加项目的庞大和复杂。

    **[⬆ 返回顶部](#目录)**

54. ### 在 React v16 中的错误边界是什么?

    错误边界是在其子组件树中的任何位置捕获 JavaScript 错误、记录这些错误并显示回退 UI 而不是崩溃的组件树的组件。

    如果一个类组件定义了一个名为 `componentDidCatch(error, info)` 或 `static getDerivedStateFromError() ` 新的生命周期方法，则该类组件将成为错误边界。

    **[⬆ 返回顶部](#目录)**

55. ### 在 React v15 中如何处理错误边界?

    React v15 使用 `unstable_handleError` 方法为错误边界提供了非常基础的支持。已在 React v16 中，将其重命名为`componentDidCatch`。 

    **[⬆ 返回顶部](#目录)**

56. ### 静态类型检查推荐的方法是什么?

    通常，我们使用 PropTypes 库（在 React v15.5 之后 `React.PropTypes` 被移动到了 `prop-types` 包中），在 React 应用程序中执行类型检查。对于大型项目，建议使用静态类型检查器，比如 Flow 或 TypeScript，它们在编译时执行类型检查并提供 auto-completion 功能。

    **[⬆ 返回顶部](#目录)**

57. ### `react-dom` 包的用途是什么?

    `react-dom` 包提供了特定的 DOM 方法，可以在应用程序的顶层使用。大多数的组件不需要使用此模块。该模块中提供的一些方法如下：

    1. `render()`
    2. `hydrate()`
    3. `unmountComponentAtNode()`
    4. `findDOMNode()`
    5. `createPortal()`

    **[⬆ 返回顶部](#目录)**

58. ### `react-dom` 中 render 方法的目的是什么?

    此方法用于将 React 元素渲染到所提供容器中的 DOM 结构中，并返回对组件的引用。如果 React 元素之前已被渲染到容器中，它将对其执行更新，并且只在需要时改变 DOM 以反映最新的更改。

    如果提供了可选的回调函数，该函数将在组件被渲染或更新后执行。

    **[⬆ 返回顶部](#目录)**

60. ### 在 React 中如何使用 innerHTML?

    `dangerouslySetInnerHTML` 属性是 React 用来替代在浏览器 DOM 中使用 `innerHTML`。与 `innerHTML` 一样，考虑到跨站脚本攻击（XSS），使用此属性也是有风险的。使用时，你只需传递以 `__html` 作为键，而 HTML 文本作为对应值的对象。

    **[⬆ 返回顶部](#目录)**

61. ### 如何在 React 中使用样式?

    `style` 属性接受含有 camelCased（驼峰）属性的 JavaScript 对象，而不是 CSS 字符串。这与 DOM 样式中的 JavaScript 属性一致，效率更高，并且可以防止 XSS 安全漏洞。

    为了与在 JavaScript 中访问 DOM 节点上的属性保持一致，样式键采用了 camelcased（例如`node.style.backgroundImage`）。

    **[⬆ 返回顶部](#目录)**


62. ### 在 React 中事件有何不同?

    处理 React 元素中的事件有一些语法差异：

    1. React 事件处理程序是采用驼峰而不是小写来命名的。 
    2. 使用 JSX，你将传递一个函数作为事件处理程序，而不是字符串。

    **[⬆ 返回顶部](#目录)**

63. ### 如果在构造函数中使用 `setState()` 会发生什么?

    当你使用 `setState()` 时，除了设置状态对象之外，React 还会重新渲染组件及其所有的子组件。你会得到这样的错误：*Can only update a mounted or mounting component.*。因此我们需要在构造函数中使用 `this.state` 初始化状态。

    **[⬆ 返回顶部](#目录)**

64. ### 索引作为键的影响是什么?

    Keys 应该是稳定的，可预测的和唯一的，这样 React 就能够跟踪元素。

    每个元素的键将基于列表项的顺序，而不是绑定到即将展示的数据上。这将限制 React 能够实现的优化。

    假设 `todo.id` 对此列表是唯一且稳定的，如果将此数据作为唯一键，那么 React 将能够对元素进行重新排序，而无需重新创建它们。 

    **[⬆ 返回顶部](#目录)**

65. ### 在 `componentWillMount()` 方法中使用 `setState()` 好吗?

    建议避免在 `componentWillMount()` 生命周期方法中执行异步初始化。在 mounting 发生之前会立即调用 `componentWillMount()`，且它在 `render()` 之前被调用，因此在此方法中更新状态将不会触发重新渲染。应避免在此方法中引入任何副作用或订阅操作。我们需要确保对组件初始化的异步调用发生在 `componentDidMount()` 中，而不是在 `componentWillMount()` 中。
  
    **[⬆ 返回顶部](#目录)**

66. ### 如果在初始状态中使用 props 属性会发生什么?

    如果在不刷新组件的情况下更改组件上的属性，则不会显示新的属性值，因为构造函数函数永远不会更新组件的当前状态。只有在首次创建组件时才会用 props 属性初始化状态。
    
    **[⬆ 返回顶部](#目录)**

67. ### 如何有条件地渲染组件?

    在某些情况下，你希望根据某些状态渲染不同的组件。 JSX 不会渲染 `false` 或 `undefined`，因此你可以使用 `&&` 运算符，在某个条件为 true 时，渲染组件中指定的内容。

    **[⬆ 返回顶部](#目录)**

68. ### 为什么在 DOM 元素上展开 props 需要小心?

    当我们展开属性时，我们会遇到添加未知 HTML 属性的风险，这是一种不好的做法。相反，我们可以使用属性解构和`...rest` 运算符，因此它只添加所需的 props 属性。

    **[⬆ 返回顶部](#目录)**

70. ### 如何 memoize（记忆）组件?

    有可用于函数组件的 memoize 库。例如 `moize` 库可以将组件存储在另一个组件中。

    **[⬆ 返回顶部](#目录)**

72. ### 如何在 React 中启用生产模式?

    你应该使用 Webpack 的 `DefinePlugin` 方法将 `NODE_ENV` 设置为 `production`，通过它你可以去除 propType 验证和额外警告等内容。除此之外，如果你压缩代码，如使用 Uglify 的死代码消除，以去掉用于开发的代码和注释，它将大大减少包的大小。

    **[⬆ 返回顶部](#目录)**

73. ### 什么是 CRA 及其好处?

    `create-react-app` CLI 工具允许你无需配置步骤，快速创建和运行 React 应用。

    它包含了构建 React 应用程序所需的一切：

    1. React, JSX, ES6, 和 Flow 语法支持。
    2. ES6 之外的语言附加功能，比如对象扩展运算符。
    3. Autoprefixed CSS，因此你不在需要 -webkit- 或其他前缀。
    4. 一个快速的交互式单元测试运行程序，内置了对覆盖率报告的支持。
    5. 一个实时开发服务器，用于警告常见错误。
    6. 一个构建脚本，用于打包用于生产中包含 hashes 和 sourcemaps 的 JS、CSS 和 Images 文件。

    **[⬆ 返回顶部](#目录)**

74. ### 在 mounting 阶段生命周期方法的执行顺序是什么?

    在创建组件的实例并将其插入到 DOM 中时，将按以下顺序调用生命周期方法。

    1. `constructor()`
    2. `static getDerivedStateFromProps()`
    3. `render()`
    4. `componentDidMount()`

    **[⬆ 返回顶部](#目录)**

75. ### 在 React v16 中，哪些生命周期方法将被弃用?

    以下生命周期方法将成为不安全的编码实践，并且在异步渲染方面会更有问题。

    1. `componentWillMount()`
    2. `componentWillReceiveProps()`
    3. `componentWillUpdate()`

    从 React v16.3 开始，这些方法使用 `UNSAFE_` 前缀作为别名，未加前缀的版本将在 React v17 中被移除。

    **[⬆ 返回顶部](#目录)**

76. ### 生命周期方法 `getDerivedStateFromProps()` 的目的是什么?

    新的静态 `getDerivedStateFromProps()` 生命周期方法在实例化组件之后以及重新渲染组件之前调用。它可以返回一个对象用于更新状态，或者返回 `null` 指示新的属性不需要任何状态更新。

    此生命周期方法与 `componentDidUpdate()` 一起涵盖了 `componentWillReceiveProps()` 的所有用例。

    **[⬆ 返回顶部](#目录)**

77. ### 生命周期方法 `getSnapshotBeforeUpdate()` 的目的是什么?

    新的 `getSnapshotBeforeUpdate()` 生命周期方法在 DOM 更新之前被调用。此方法的返回值将作为第三个参数传递给`componentDidUpdate()`。

    此生命周期方法与 `componentDidUpdate()` 一起涵盖了 `componentWillUpdate()` 的所有用例。

    **[⬆ 返回顶部](#目录)**

78. ### createElement() 和 cloneElement() 方法有什么区别?

    JSX 元素将被转换为 `React.createElement()` 函数来创建 React 元素，这些对象将用于表示 UI 对象。而 `cloneElement` 用于克隆元素并传递新的属性。

    **[⬆ 返回顶部](#目录)**

80. ### 在组件类中方法的推荐顺序是什么?

    从 *mounting* 到 *render stage* 阶段推荐的方法顺序：

    1. `static` 方法
    2. `constructor()`
    3. `getChildContext()`
    4. `componentWillMount()`
    5. `componentDidMount()`
    6. `componentWillReceiveProps()`
    7. `shouldComponentUpdate()`
    8. `componentWillUpdate()`
    9. `componentDidUpdate()`
    10. `componentWillUnmount()`
    11. 点击处理程序或事件处理程序，如 `onClickSubmit()` 或 `onChangeDescription()`
    12. 用于渲染的getter方法，如 `getSelectReason()` 或 `getFooterContent()`
    13. 可选的渲染方法，如 `renderNavigation()` 或 `renderProfilePicture()`
    14. `render()`

    **[⬆ 返回顶部](#目录)**

81. ### 什么是 switching 组件?

    switching 组件是渲染多个组件之一的组件。我们需要使用对象将 prop 映射到组件中。

    例如，以下的 switching 组件将基于 `page` 属性显示不同的页面。

    **[⬆ 返回顶部](#目录)**

82. ### 为什么我们需要将函数传递给 setState() 方法?

    这背后的原因是 `setState()` 是一个异步操作。出于性能原因，React 会对状态更改进行批处理，因此在调用 `setState()` 方法之后，状态可能不会立即更改。这意味着当你调用 `setState()` 方法时，你不应该依赖当前状态，因为你不能确定当前状态应该是什么。这个问题的解决方案是将一个函数传递给 `setState()`，该函数会以上一个状态作为参数。通过这样做，你可以避免由于 `setState()` 的异步性质而导致用户在访问时获取旧状态值的问题。

    假设初始计数值为零。在连续三次增加操作之后，该值将只增加一个。

    **[⬆ 返回顶部](#目录)**

83. ### 在 React 中什么是严格模式?

    `React.StrictMode` 是一个有用的组件，用于突出显示应用程序中的潜在问题。就像 `<Fragment>`，`<StrictMode>` 一样，它们不会渲染任何额外的 DOM 元素。它为其后代激活额外的检查和警告。这些检查仅适用于开发模式。

    在上面的示例中，*strict mode* 检查仅应用于 `<ComponentOne>` 和 `<ComponentTwo>` 组件。

    **[⬆ 返回顶部](#目录)**

84. ### React Mixins 是什么?

    *Mixins* 是一种完全分离组件通用功能的方法。 Mixins 不应该被继续使用，可以用高阶组件或装饰器来替换。

    最常用的 mixins 是 `PureRenderMixin`。当 props 和状态与之前的 props 和状态相等时，你可能在某些组件中使用它来防止不必要的重新渲染。

    **[⬆ 返回顶部](#目录)**

87. ### 为什么组件名称应该以大写字母开头?

    如果使用 JSX 渲染组件，则该组件的名称必须以大写字母开头，否则 React 将会抛出无法识别标签的错误。这种约定是因为只有 HTML 元素和 SVG 标签可以以小写字母开头。

    定义组件类的时候，你可以以小写字母开头，但在导入时应该使用大写字母。

    **[⬆ 返回顶部](#目录)**

89. ### constructor 和 getInitialState 有什么区别?

    当使用 ES6 类时，你应该在构造函数中初始化状态，而当你使用 `React.createClass()` 时，就需要使用 `getInitialState()` 方法。

    **[⬆ 返回顶部](#目录)**

90. ### 是否可以在不调用 setState 方法的情况下，强制组件重新渲染?

    默认情况下，当组件的状态或属性改变时，组件将重新渲染。如果你的 `render()` 方法依赖于其他数据，你可以通过调用 `forceUpdate()` 来告诉 React，当前组件需要重新渲染。

    建议避免使用 `forceUpdate()`，并且只在 `render()` 方法中读取 `this.props` 和 `this.state`。

    **[⬆ 返回顶部](#目录)**

97. ### 为什么 ReactDOM 从 React 分离出来?

    React 团队致力于将所有的与 DOM 相关的特性抽取到一个名为 ReactDOM 的独立库中。React v0.14 是第一个拆分后的版本。通过查看一些软件包，`react-native`，`react-art`，`react-canvas`，和 `react-three`，很明显，React 的优雅和本质与浏览器或 DOM 无关。为了构建更多 React 能应用的环境，React 团队计划将主要的 React 包拆分成两个：`react` 和 `react-dom`。这为编写可以在 React 和 React Native 的 Web 版本之间共享的组件铺平了道路。

    **[⬆ 返回顶部](#目录)**

102. ### 如何监听状态变化?

     当状态更改时将调用以下生命周期方法。你可以将提供的状态和属性值与当前状态和属性值进行比较，以确定是否发生了有意义的改变。

     ```
     componentWillUpdate(object nextProps, object nextState)
     componentDidUpdate(object prevProps, object prevState)
     ```

     **[⬆ 返回顶部](#目录)**

106. ### 为什么你不能更新 React 中的 props?

     React 的哲学是 props 应该是 *immutable* 和 *top-down*。这意味着父级可以向子级发送任何属性值，但子级不能修改接收到的属性。

     **[⬆ 返回顶部](#目录)**

118. ### 为什么 React 组件名称必须以大写字母开头?

     在 JSX 中，小写标签被认为是 HTML 标签。但是，含有 `.` 的大写和小写标签名却不是。

     1. `<component />` 将被转换为 `React.createElement('component')` (i.e, HTML 标签)
     2. `<obj.component />` 将被转换为 `React.createElement(obj.component)`
     3. `<Component />` 将被转换为 `React.createElement(Component)`

     **[⬆ 返回顶部](#目录)**

119. ### 为什么组件的构造函数只被调用一次?

     React 协调算法假设如果自定义组件出现在后续渲染的相同位置，则它与之前的组件相同，因此重用前一个实例而不是创建新实例。

     **[⬆ 返回顶部](#目录)**

125. ### 模块化样式文件有什么好处?

     建议避免在组件中对样式值进行硬编码。任何可能在不同的 UI 组件之间使用的值都应该提取到它们自己的模块中。

     **[⬆ 返回顶部](#目录)**

127. ### 如何发起 AJAX 调用以及应该在哪些组件生命周期方法中进行 AJAX 调用?

     你可以使用 AJAX 库，如 Axios，jQuery AJAX 和浏览器内置的 `fetch` API。你应该在 `componentDidMount()` 生命周期方法中获取数据。这样当获取到数据的时候，你就可以使用 `setState()` 方法来更新你的组件。

     **[⬆ 返回顶部](#目录)**

## React Router

129. ### 什么是 React Router?

     React Router 是一个基于 React 之上的强大路由库，可以帮助您快速地向应用添加视图和数据流，同时保持 UI 与 URL 同步。

     **[⬆ 返回顶部](#目录)**

130. ### React Router 与 history 库的区别?

     React Router 是`history`库的包装器，它处理浏览器的`window.history`与浏览器和哈希历史的交互。它还提供了内存历史记录，这对于没有全局历史记录的环境非常有用，例如移动应用程序开发（React Native）和使用 Node 进行单元测试。

     **[⬆ 返回顶部](#目录)**

131. ### 在 React Router v4 中的`<Router>`组件是什么?

     React Router v4 提供了以下三种类型的 `<Router>` 组件:

     1. `<BrowserRouter>`
     2. `<HashRouter>`
     3. `<MemoryRouter>`

     以上组件将创建*browser*，*hash*和*memory*的 history 实例。React Router v4 通过`router`对象中的上下文使与您的路由器关联的`history`实例的属性和方法可用。

     **[⬆ 返回顶部](#目录)**

132. ### `history` 中的 `push()` 和 `replace()` 方法的目的是什么?

     一个 history 实例有两种导航方法：

     1. `push()`
     2. `replace()`

     如果您将 history 视为一个访问位置的数组，则`push()`将向数组添加一个新位置，`replace()`将用新的位置替换数组中的当前位置。

     **[⬆ 返回顶部](#目录)**

137. ### 如何实现默认页面或 404 页面?

     `<Switch>`呈现匹配的第一个孩子`<Route>`。 没有路径的`<Route>`总是匹配。所以你只需要简单地删除 path 属性，如下所示：

     **[⬆ 返回顶部](#目录)**

139. ### 登录后如何执行自动重定向?

     `react-router`包在 React Router 中提供了`<Redirect>`组件。渲染`<Redirect>`将导航到新位置。与服务器端重定向一样，新位置将覆盖历史堆栈中的当前位置。

     **[⬆ 返回顶部](#目录)**

## React Redux

152. ### 什么是 Flux?

     *Flux* 是*应用程序设计范例*，用于替代更传统的 MVC 模式。它不是一个框架或库，而是一种新的体系结构，它补充了 React 和单向数据流的概念。在使用 React 时，Facebook 会在内部使用此模式。

     在 dispatcher，stores 和视图组件具有如下不同的输入和输出：

     ![flux](images/flux.png)

     **[⬆ 返回顶部](#目录)**

153. ### 什么是 Redux?

     *Redux* 是基于 *Flux设计模式* 的 JavaScript 应用程序的可预测状态容器。Redux 可以与 React 一起使用，也可以与任何其他视图库一起使用。它很小（约2kB）并且没有依赖性。

     **[⬆ 返回顶部](#目录)**

154. ### Redux 的核心原则是什么？?

     Redux 遵循三个基本原则：

     1. **单一数据来源：** 整个应用程序的状态存储在单个对象树中。单状态树可以更容易地跟踪随时间的变化并调试或检查应用程序。
     2. **状态是只读的：** 改变状态的唯一方法是发出一个动作，一个描述发生的事情的对象。这可以确保视图和网络请求都不会直接写入状态。
     3. **使用纯函数进行更改：** 要指定状态树如何通过操作进行转换，您可以编写reducers。Reducers 只是纯函数，它将先前的状态和操作作为参数，并返回下一个状态。

     **[⬆ 返回顶部](#目录)**

155. ### 与 Flux 相比，Redux 的缺点是什么?

     我们应该说使用 Redux 而不是 Flux 几乎没有任何缺点。这些如下：

     1. **您将需要学会避免突变：** Flux 对变异数据毫不吝啬，但 Redux 不喜欢突变，许多与 Redux 互补的包假设您从不改变状态。您可以使用 dev-only 软件包强制执行此操作，例如`redux-immutable-state-invariant`，Immutable.js，或指示您的团队编写非变异代码。
     2. **您将不得不仔细选择您的软件包：** 虽然 Flux 明确没有尝试解决诸如撤消/重做，持久性或表单之类的问题，但 Redux 有扩展点，例如中间件和存储增强器，以及它催生了丰富的生态系统。
     3. **还没有很好的 Flow 集成：** Flux 目前可以让你做一些非常令人印象深刻的静态类型检查，Redux 还不支持。

     **[⬆ 返回顶部](#目录)**

157. ### 我可以在 reducer 中触发一个 Action 吗?

     在 reducer 中触发 Action 是**反模式**。您的 reducer 应该*没有副作用*，只是接收 Action 并返回一个新的状态对象。在 reducer 中添加侦听器和调度操作可能会导致链接的 Action 和其他副作用。

     **[⬆ 返回顶部](#目录)**

163. ### 如何在 Redux 中重置状态?

     你需要在你的应用程序中编写一个*root reducer*，它将处理动作委托给`combineReducers()`生成的 reducer。

     例如，让我们在`USER_LOGOUT`动作之后让`rootReducer()`返回初始状态。我们知道，无论 Action 怎么样，当使用`undefined`作为第一个参数调用它们时，reducers 应该返回初始状态。

     ```javascript
     const appReducer = combineReducers({
       /* your app's top-level reducers */
     })

     const rootReducer = (state, action) => {
       if (action.type === 'USER_LOGOUT') {
         state = undefined
       }

       return appReducer(state, action)
     }
     ```

     如果使用`redux-persist`，您可能还需要清理存储空间。`redux-persist`在 storage 引擎中保存您的状态副本。首先，您需要导入适当的 storage 引擎，然后在将其设置为`undefined`之前解析状态并清理每个存储状态键。

     ```javascript
     const appReducer = combineReducers({
       /* your app's top-level reducers */
     })

     const rootReducer = (state, action) => {
       if (action.type === 'USER_LOGOUT') {
         Object.keys(state).forEach(key => {
           storage.removeItem(`persist:${key}`)
         })

         state = undefined
       }

       return appReducer(state, action)
     }
     ```

     **[⬆ 返回顶部](#目录)**

165. ### React 上下文和 React Redux 之间有什么区别?

     您可以直接在应用程序中使用**Context**，这对于将数据传递给深度嵌套的组件非常有用。而**Redux**功能更强大，它还提供了 Context API 无法提供的大量功能。此外，React Redux 在内部使用上下文，但它不会在公共 API 中有所体现。

     **[⬆ 返回顶部](#目录)**

166. ### 为什么 Redux 状态函数称为 reducers ?

     Reducers 总是返回状态的累积（基于所有先前状态和当前 Action）。因此，它们充当了状态的 Reducer。每次调用 Redux reducer 时，状态和 Action 都将作为参数传递。然后基于该 Action 减少（或累积）该状态，然后返回下一状态。您可以*reduce*一组操作和一个初始状态（Store），在该状态下执行这些操作以获得最终的最终状态。

     **[⬆ 返回顶部](#目录)**

168. ### 我应该在 Redux Store 中保留所有组件的状态吗?

      将数据保存在 Redux 存储中，并在组件内部保持 UI 相关状态。

      **[⬆ 返回顶部](#目录)**

170. ### React Redux 中展示组件和容器组件之间的区别是什么?

     **展示组件**是一个类或功能组件，用于描述应用程序的展示部分。

     **容器组件**是连接到 Redux Store的组件的非正式术语。容器组件*订阅* Redux 状态更新和*dispatch*操作，它们通常不呈现 DOM 元素；他们将渲染委托给展示性的子组件。

     **[⬆ 返回顶部](#目录)**

174. ### Redux 中的 Action 是什么?

     *Actions*是纯 JavaScript 对象或信息的有效负载，可将数据从您的应用程序发送到您的 Store。 它们是 Store 唯一的数据来源。 Action 必须具有指示正在执行的操作类型的 type 属性。

     **[⬆ 返回顶部](#目录)**

175. ### 什么是 redux-saga?

     `redux-saga`是一个库，旨在使 React/Redux 项目中的副作用（数据获取等异步操作和访问浏览器缓存等可能产生副作用的动作）更容易，更好。

     **[⬆ 返回顶部](#目录)**

176. ### redux-saga 的模型概念是什么?

     *Saga*就像你的项目中的一个单独的线程，它独自负责副作用。`redux-saga` 是一个 redux *中间件*，这意味着它可以在项目启动中使用正常的 Redux 操作，暂停和取消该线程，它可以访问完整的 Redux 应用程序状态，并且它也可以调度 Redux 操作。

     **[⬆ 返回顶部](#目录)**

177. ### 在 redux-saga 中 `call()` 和 `put()` 之间有什么区别?

     `call()`和`put()`都是 Effect 创建函数。 `call()`函数用于创建 Effect 描述，指示中间件调用 promise。`put()`函数创建一个 Effect，指示中间件将一个 Action 分派给 Store。

     **[⬆ 返回顶部](#目录)**

178. ### 什么是 Redux Thunk?

     *Redux Thunk*中间件允许您编写返回函数而不是 Action 的创建者。 thunk 可用于延迟 Action 的发送，或仅在满足某个条件时发送。内部函数接收 Store 的方法`dispatch()`和`getState()`作为参数。

     **[⬆ 返回顶部](#目录)**

179. ### `redux-saga` 和 `redux-thunk` 之间有什么区别?

     *Redux Thunk*和*Redux Saga*都负责处理副作用。在大多数场景中，Thunk 使用*Promises*来处理它们，而 Saga 使用*Generators*。Thunk 易于使用，因为许多开发人员都熟悉 Promise，Sagas/Generators 功能更强大，但您需要学习它们。但是这两个中间件可以共存，所以你可以从 Thunks 开始，并在需要时引入 Sagas。

     **[⬆ 返回顶部](#目录)**

180. ### 什么是 Redux DevTools?

     *Redux DevTools*是 Redux 的实时编辑的时间旅行环境，具有热重新加载，Action 重放和可自定义的 UI。如果您不想安装 Redux DevTools 并将其集成到项目中，请考虑使用 Chrome 和 Firefox 的扩展插件。

     **[⬆ 返回顶部](#目录)**

181. ### Redux DevTools 的功能有哪些?

     1. 允许您检查每个状态和 action 负载。
     2. 让你可以通过*撤销*回到过去。
     3. 如果更改 reducer 代码，将重新评估每个*已暂存*的 Action。
     4. 如果 Reducers 抛出错误，你会看到这发生了什么 Action，以及错误是什么。
     5. 使用`persistState()`存储增强器，您可以在页面重新加载期间保持调试会话。

     **[⬆ 返回顶部](#目录)**

199. ### 与 Vue.js 相比，React 有哪些优势?

     与 Vue.js 相比，React 具有以下优势：

     1. 在大型应用程序开发中提供更大的灵活性。
     2. 更容易测试。
     3. 更适合创建移动端应用程序。
     4. 提供更多的信息和解决方案。

     **[⬆ 返回顶部](#目录)**

202. ### 什么是 Styled Components?

     styled-components 是一个用于样式化 React 应用程序的 JavaScript 库。 它删除了样式和组件之间的映射，并允许您在 js 中编写 CSS。

     **[⬆ 返回顶部](#目录)**

210. ### Redux 只能与 React 一起使用么?

     Redux 可以用做任何 UI 层的数据存储。最常见的应用场景是 React 和 React Native，但也有一些 bindings 可用于 AngularJS，Angular 2，Vue，Mithril 等项目。Redux 只提供了一种订阅机制，任何其他代码都可以使用它。

     **[⬆ 返回顶部](#目录)**

216. ### 在 React 中什么是渲染劫持?

     渲染劫持的概念是控制一个组件将从另一个组件输出什么的能力。实际上，这意味着你可以通过将组件包装成高阶组件来装饰组件。通过包装，你可以注入额外的属性或产生其他变化，这可能会导致渲染逻辑的更改。实际上它不支持劫持，但通过使用 HOC，你可以使组件以不同的方式工作。

     **[⬆ 返回顶部](#目录)**

221. ### React memo 函数是什么?

     当类组件的输入属性相同时，可以使用 **pureComponent** 或 **shouldComponentUpdate** 来避免组件的渲染。现在，你可以通过把函数组件包装在 **React.memo** 中来实现相同的功能。

     **[⬆ 返回顶部](#目录)**

222. ### React lazy 函数是什么?

     使用 React.lazy 函数允许你将动态导入的组件作为常规组件进行渲染。当组件开始渲染时，它会自动加载包含 OtherComponent 的包。它必须返回一个 Promise，该 Promise 解析后为一个带有默认导出 React 组件的模块。

     **注意：** React.lazy 和 Suspense 还不能用于服务端渲染。如果要在服务端渲染的应用程序中进行代码拆分，我们仍然建议使用 React Loadable。

     **[⬆ 返回顶部](#目录)**

223. ### 如何使用 setState 防止不必要的更新?

     你可以把状态的当前值与已有的值进行比较，并决定是否重新渲染页面。如果没有更改，你需要返回 `null` 以阻止渲染，否则返回最新的状态值。



     **[⬆ 返回顶部](#目录)**

229. ### Flux 和 Redux 之间有什么区别?

     以下是 Flux 和 Redux 之间的主要区别

     | Flux | Redux |
     | ----- | ------- |
     | 状态是可变的 | 状态是不可变的 |
     | Store 包含状态和更改逻辑 | 存储和更改逻辑是分开的 |
     | 存在多个 Store | 仅存在一个 Store |
     | 所有的 Store 都是断开连接的 | 带有分层 reducers 的 Store |
     | 它有一个单独的 dispatcher | 没有 dispatcher 的概念 |
     | React 组件监测 Store | 容器组件使用连接函数 |

     **[⬆ 返回顶部](#目录)**

231. ### 您能描述一下 componentDidCatch 生命周期方法签名吗?

     在后代层级的组件抛出错误后，将调用**componentDidCatch**生命周期方法。该方法接收两个参数：

     1. error: - 抛出的错误对象
     2. info: - 具有 componentStack 键的对象，包含有关哪个组件引发错误的信息。

     **[⬆ 返回顶部](#目录)**

232. ### 在哪些情况下，错误边界不会捕获错误?

     以下是错误边界不起作用的情况：

     1. 在事件处理器内。
     2. **setTimeout** 或 **requestAnimationFrame** 回调中的异步代码。
     3. 在服务端渲染期间。
     4. 错误边界代码本身中引发错误时。

     **[⬆ 返回顶部](#目录)**

240. ### 构造函数的主要目的是什么?

     使用构造函数主要有两个目的：

     1. 通过将对象分配给 this.state 来初始化本地状态。
     2. 用于为组件实例绑定事件处理方法。

     **[⬆ 返回顶部](#目录)**

243. ### 为什么不能在 componentWillUnmount 中调用 setState() 方法?

     不应在 componentWillUnmount() 中调用 setState()，因为一旦卸载了组件实例，就永远不会再次装载它。

     **[⬆ 返回顶部](#目录)**

245. ### 当组件重新渲染时顺序执行的方法有哪些?

     更新可能由属性或状态的更改引起。在重新渲染组件时，会按以下顺序调用下列方法。

     1. static getDerivedStateFromProps()
     2. shouldComponentUpdate()
     3. render()
     4. getSnapshotBeforeUpdate()
     5. componentDidUpdate()

     **[⬆ 返回顶部](#目录)**

246. ### 错误处理期间调用哪些方法?

     在渲染期间，生命周期方法内或任何子组件的构造函数中出现错误时，将会调用以下方法：

     1. static getDerivedStateFromError()
     2. componentDidCatch()

     **[⬆ 返回顶部](#目录)**

250. ### 什么是代码拆分?

     Code-Splitting 是 Webpack 和 Browserify 等打包工具所支持的一项功能，它可以创建多个 bundles，并可以在运行时动态加载。React 项目支持通过 dynamic import() 特性进行代码拆分。例如，在下面的代码片段中，它将使 moduleA.js 及其所有唯一依赖项作为单独的块，仅当用户点击 'Load' 按钮后才加载。

     **[⬆ 返回顶部](#目录)**

251. ### 严格模式有什么好处?

     在下面的情况下，<StrictMode> 将有所帮助：

     1. 使用 **unsafe lifecycle methods** 标识组件。
     2. 有关 **legacy string ref** API 用法发出警告。
     3. 检测无法预测的 **side effects**。
     4. 检测 **legacy context** API。
     5. 有关已弃用的 findDOMNode 用法的警告。

     **[⬆ 返回顶部](#目录)**

252. ### 什么是 Keyed Fragments ?

     使用显式 <React.Fragment> 语法声明的片段可能具有 key 。一般用例是将集合映射到片段数组，如下所示，

     **注意：** 键是唯一可以传递给 Fragment 的属性。将来，可能会支持其他属性，例如事件处理程序。

     **[⬆ 返回顶部](#目录)**

254. ### HOC 有哪些限制?

     除了它的好处之外，高阶组件还有一些注意事项。 以下列出的几个注意事项:
     1. **不要在渲染方法中使用HOC：**
        建议不要将 HOC 应用于组件的 render 方法中的组件。
        ```javascript
        render() {
          // A new version of EnhancedComponent is created on every render
          // EnhancedComponent1 !== EnhancedComponent2
          const EnhancedComponent = enhance(MyComponent);
          // That causes the entire subtree to unmount/remount each time!
          return <EnhancedComponent />;
        }
        ```
        上述代码通过重新装载，将导致该组件及其所有子组件状态丢失，会影响到性能。正确的做法应该是在组件定义之外应用 HOC ，以便仅生成一次生成的组件

     2. **静态方法必须复制：**
        将 HOC 应用于组件时，新组件不具有原始组件的任何静态方法
        ```javascript
        // Define a static method
        WrappedComponent.staticMethod = function() {/*...*/}
        // Now apply a HOC
        const EnhancedComponent = enhance(WrappedComponent);

        // The enhanced component has no static method
        typeof EnhancedComponent.staticMethod === 'undefined' // true
        ```
        您可以通过在返回之前将方法复制到输入组件上来解决此问题
        ```javascript
        function enhance(WrappedComponent) {
          class Enhance extends React.Component {/*...*/}
          // Must know exactly which method(s) to copy :(
          Enhance.staticMethod = WrappedComponent.staticMethod;
          return Enhance;
        }
        ```
     3. **Refs 不会被往下传递**
        对于HOC，您需要将所有属性传递给包装组件，但这对于 refs 不起作用。这是因为 ref 并不是一个类似于 key 的属性。在这种情况下，您需要使用 React.forwardRef API。

     **[⬆ 返回顶部](#目录)**

260. ### 如何防止函数被多次调用?

     如果你使用一个事件处理程序，如 **onClick or onScroll** 并希望防止回调被过快地触发，那么你可以限制回调的执行速度。

     这可以通过以下可能的方式实现：

     1. **Throttling:** 基于时间的频率进行更改。例如，它可以使用 lodash 的 _.throttle 函数。
     2. **Debouncing:** 在一段时间不活动后发布更改。例如，可以使用 lodash 的 _.debounce 函数。
     3. **RequestAnimationFrame throttling:** 基于 requestAnimationFrame 的更改。例如，可以使用 raf-schd。

     > 注意：_.debounce， _.throttle 和 raf-schd 都提供了一个 cancel 方法来取消延迟回调。所以需要调用 componentWillUnmount，或者对代码进行检查来保证在延迟函数有效期间内组件始终挂载。

     **[⬆ 返回顶部](#目录)**

261. ### JSX 如何防止注入攻击?

     React DOM 会在渲染 JSX 中嵌入的任何值之前对其进行转义。因此，它确保你永远不能注入任何未在应用程序中显式写入的内容。

     ```javascript
     const name = response.potentiallyMaliciousInput;
     const element = <h1>{name}</h1>;
     ```

     这样可以防止应用程序中的XSS（跨站点脚本）攻击。

     **[⬆ 返回顶部](#目录)**

263. ### 你怎么说 props 是只读的?

     当你将组件声明为函数或类时，它决不能修改自己的属性。让我们来实现一个 capital 的函数：

     ```javascript
     function capital(amount, interest) {
        return amount + interest;
     }
     ```

     上面的函数称为“纯”函数，因为它不会尝试更改输入，并总是为相同的输入返回相同的结果。因此，React 有一条规则，即“所有 React 组件的行为都必须像纯函数一样”。

     **[⬆ 返回顶部](#目录)**

274. ### 什么是 loadable 组件?

     如果你想要在服务端渲染的应用程序中实现代码拆分，建议使用 Loadable 组件，因为 React.lazy 和 Suspense 还不可用于服务器端渲染。Loadable 允许你将动态导入的组件作为常规的组件进行渲染。
     现在，其他组件将以单独的包进行加载。

     **[⬆ 返回顶部](#目录)**

276. ### 什么是基于路由的代码拆分?

     进行代码拆分的最佳位置之一是路由。整个页面将立即重新渲染，因此用户不太可能同时与页面中的其他元素进行交互。因此，用户体验不会受到干扰。

     **[⬆ 返回顶部](#目录)**

277. ### 举例说明如何使用 context?

     **Context** 旨在共享可被视为全局的数据，用于 React 组件树。例如，在下面的代码中，允许手动通过一个 theme 属性来设置按钮组件的样式。

     **[⬆ 返回顶部](#目录)**

278. ### 在 context 中默认值的目的是什么?

     当在组件树中的组件没有匹配到在其上方的 Provider 时，才会使用 defaultValue 参数。这有助于在不包装组件的情况下单独测试组件。

     **[⬆ 返回顶部](#目录)**

280. ### 什么是 consumer?

     Consumer 是一个订阅上下文更改的 React 组件。它需要一个函数作为子元素，该函数接收当前上下文的值作为参数，并返回一个 React 元素。传递给函数 value 参数的参数值将等于在组件树中当前组件最近的 Provider 元素的 value 属性值。

     **[⬆ 返回顶部](#目录)**

281. ### 在使用 context 时，如何解决性能方面的问题?

     Context 使用引用标识来确定何时重新渲染，当 Provider 的父元素重新渲染时，会有一些问题即可能会在 Consumers 中触发无任何意图的渲染。每次 Provider 重新渲染时，重新渲染所有的 Consumers，这是因为渲染 Provider 时，始终会为 value 属性创建一个新的对象。

     **[⬆ 返回顶部](#目录)**

282. ### 在 HOCs 中 forward ref 的目的是什么?

     因为 ref 不是一个属性，所以 Refs 不会被传递。就像 **key** 一样，React 会以不同的方式处理它。如果你将 ref 添加到 HOC，则该 ref 将引用最外层的容器组件，而不是包装的组件。在这种情况下，你可以使用 Forward Ref API。例如，你可以使用 React.forwardRef API 显式地将 refs 转发的内部的 FancyButton 组件。

     **[⬆ 返回顶部](#目录)**

287. ### 什么是差异算法? 

     React 需要使用算法来了解如何有效地更新 UI 以匹配最新的树。差异算法将生成将一棵树转换为另一棵树的最小操作次数。然而，算法具有 O(n3) 的复杂度，其中 n 是树中元素的数量。在这种情况下，对于显示 1000 个元素将需要大约 10 亿个比较。这太昂贵了。相反，React 基于两个假设实现了一个复杂度为 O(n) 的算法：

     1. 两种不同类型的元素会产生不同的树结构。
     2. 开发者可以通过一个 key 属性，标识哪些子元素可以在不同渲染中保持稳定。

     **[⬆ 返回顶部](#目录)**

288. ### 差异算法涵盖了哪些规则?

     在区分两棵树时，React 首先比较两个根元素。根据根元素的类型，行为会有所不同。它在重构算法中涵盖了以下规则：

     1. **不同类型的元素：**
        每当根元素具有不同的类型时，React 将移除旧树并从头开始构建新树。例如，元素 <a> 到 <img>，或从 <Article> 到 <Comment> 的不同类型的元素引导完全重建。

     2. **相同类型的DOM元素：**
        当比较两个相同类型的 React DOM 元素时，React 查看两者的属性，保持相同的底层 DOM 节点，并仅更新已更改的属性。让我们以相同的 DOM 元素为例，除了 className 属性，

        ```javascript
        <div className="show" title="ReactJS" />

        <div className="hide" title="ReactJS" />
        ```

     3. **相同类型的组件元素：**

        当组件更新时，实例保持不变，以便在渲染之间保持状态。React 更新底层组件实例的 props 以匹配新元素，并在底层实例上调用 componentWillReceiveProps() 和 componentWillUpdate()。之后，调用 render() 方法，diff 算法对前一个结果和新结果进行递归。

     4. **递归子节点：**
        当对 DOM 节点的子节点进行递归时，React 会同时迭代两个子节点列表，并在出现差异时生成变异。例如，在子节点末尾添加元素时，在这两个树之间进行转换效果很好。

        ```javascript
        <ul>
          <li>first</li>
          <li>second</li>
        </ul>

        <ul>
          <li>first</li>
          <li>second</li>
          <li>third</li>
        </ul>

        ```
     5. **处理 Key：**

     React支持 key 属性。当子节点有 key 时，React 使用 key 将原始树中的子节点与后续树中的子节点相匹配。例如，添加 key 可以使树有效地转换，

     ```javascript
     <ul>
       <li key="2015">Duke</li>
       <li key="2016">Villanova</li>
     </ul>
     
     <ul>
       <li key="2014">Connecticut</li>
       <li key="2015">Duke</li>
       <li key="2016">Villanova</li>
     </ul>
     ```

     **[⬆ 返回顶部](#目录)**

289. ### 你什么时候需要使用 refs?

     这里是 refs 的一些使用场景：

     1. 管理聚焦、文本选择或媒体播放。
     2. 触发命令式动画。
     3. 与第三方 DOM 库集成。

     **[⬆ 返回顶部](#目录)**

291. ### 在 Pure Component 中使用渲染属性会有什么问题?

     如果在渲染方法中创建函数，则会否定纯组件的用途。因为浅属性比较对于新属性总是返回 false，在这种情况下，每次渲染都将为渲染属性生成一个新值。你可以通过将渲染函数定义为实例方法来解决这个问题。

     **[⬆ 返回顶部](#目录)**

292. ### 如何使用渲染属性创建 HOC?

     可以使用带有渲染属性的常规组件实现大多数高阶组件（HOC）。例如，如果希望使用 withMouse HOC 而不是 `<Mouse>` 组件，则你可以使用带有渲染属性的常规 `<Mouse>` 组件轻松创建一个 HOC 组件。

     **[⬆ 返回顶部](#目录)**

293. ### 什么是 windowing 技术?

     Windowing 是一种技术，它在任何给定时间只呈现一小部分行，并且可以显著减少重新呈现组件所需的时间以及创建的 DOM 节点的数量。如果应用程序呈现长的数据列表，则建议使用此技术。react-window 和 react-virtualized 都是常用的 windowing 库，它提供了几个可重用的组件，用于显示列表、网格和表格数据。

     **[⬆ 返回顶部](#目录)**

296. ### 如何设置非受控组件的默认值?

     在 React 中，表单元素的属性值将覆盖其 DOM 中的值。对于非受控组件，你可能希望能够指定其初始值，但不会控制后续的更新。要处理这种情形，你可以指定一个 **defaultValue** 属性来取代 **value** 属性。

     这同样适用于 `select` 和 `textArea` 输入框。但对于 `checkbox` 和 `radio` 控件，需要使用 **defaultChecked**。

     **[⬆ 返回顶部](#目录)**

297. ### 你最喜欢的 React 技术栈是什么?

     尽管技术栈因开发人员而异，但最流行的技术栈用于 React boilerplate 项目代码中。它主要使用 redux 和 redux saga 进行状态管理和具有副作用的异步操作，使用 react-router 进行路由管理，使用 styled-components 库开发 React 组件，使用 axios 调用 REST api，以及其他支持的技术栈，如 webpack、reseselect、esnext、babel 等。

     **[⬆ 返回顶部](#目录)**

298. ### Real DOM 和 Virtual DOM 有什么区别?
     以下是Real DOM和Virtual DOM之间的主要区别：

     | Real DOM | Virtual DOM |
     | ----- | ------- |
     | 更新速度慢 | 更新速度快 |
     | DOM 操作非常昂贵 | DOM 操作非常简单 |
     | 可以直接更新 HTML | 你不能直接更新 HTML |
     | 造成太多内存浪费 | 更少的内存消耗 |
     | 如果元素更新了，创建新的 DOM 节点 | 如果元素更新，则更新 JSX 元素 |

     **[⬆ 返回顶部](#目录)**
