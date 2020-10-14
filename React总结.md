#### React 技术栈
```
    1. yarn  Facebook开发的node package管理工具。
    2. babel 能够把ES6、ES7转成ES5的工具；使用最新的JavaScript语言标准来开发，体验新标准带来的语法糖与便利。
    3. webpack  项目打包工具，可以结合babel实现ES6/7转码成ES5，还能实现代码热更新，SASS/LESS样式处理，图片资源处理等。
    4. eslint  代码风格管理，统一团队代码风格很重要
    5. react   当前最流行的WEB前端开发框架，由Facebook开源。
    6. redux 结合react使用，通过Action改变Store，再由Store更新Component。
    7. redux-saga 结合redux使用，通过监听Action处理任务，能够实现流程化，是一个很强大的库。
    8. axios http请求库。
    10. less
    11. antd
    12. antv

```

#### 为什么选择react
```
react属于V层框架，数据与视图分离，在数据规模比较大 的项目会比较便捷。而且react有着虚拟dom、diff渲染，性能高效的优势
组件化，在传统的项目分工中，一般是以页面级别去分工，看似合理。但是react可以以组件化的方式去分工，更加碎片化。例如一个大的业务区，可以拆分除不同的组件存在，合理分工开发。
自律规范化，有着自己的生命周期，生命周期职责明确。
多端统一，可以一套代码多端使用。
react周边生态丰富
```
#### react和vue的区别
```
- 相同点：
    1. 数据驱动页面，提供响应式的视图组件
    2. 都有虚拟DOM,组件化的开发，通过props参数进行父子之间组件传递数据，都实现了webComponents规范
    3. 数据流动单向，都支持服务器的渲染SSRse
- 不同点：
    1. 数据绑定：Vue实现了双向的数据绑定，react数据流动是单向的
    2. 数据渲染：大规模的数据渲染，react更快
    3. 使用场景：React配合Redux架构适合大规模多人协作复杂项目，Vue适合小快的项目
    4. 模板和jsx:vue推荐你去写近似常规HTML的模板，React推荐你所有的模板通用JavaScript的语法扩展JSX书写
    5. 状态管理和数据对象：在vue中，数据由data属性在Vue对象中进行管理。React通过state进行状态管理
    
```

#### 真实DOM和虚拟DOM的区别
```
- 真实DOM：是直接更新 HTML, 如果元素更新，则创建新DOM，所以DOM操作代价很⾼，消耗的内存也比较多，更新也比较缓慢
- 虚拟DOM： ⽆法直接更新 HTML，如果元素更新，则更新 JSX，DOM 操作⾮常简单，所以很少的内存消耗，更新也更快
* 为什么不直接操作真实DOM===>会触发页面的重绘和回流。
```
#### 什么是 React Fiber
```
- Fiber 是 React 16 中新的协调引擎或重新实现核心算法。它的主要目标是支持虚拟DOM的增量渲染。提高其在动画、布局、手势、暂停、中止或重用等方面的适用性，并为不同类型的更新分配优先级，以及新的并发原语。它的主要特性是增量渲染:能够将渲染工作分割成块，并将其分散到多个帧中。
```
#### React Fiber算法
```
1. 解决的问题：当组件树很大的时候，因为更新过程是同步地一层组件套一层组件，逐渐深入的过程，在更新完所有组件之前不停止，函数的调用栈调用得很深，而且很长时间不会返回。
2. 解决的方式：把一个耗时长的任务分成很多小片，每一个小片的运行时间很短，虽然总时间依然很长，但是在每个小片执行完之后，都给其他任务一个执行的机会，这样唯一的线程就不会被独占，其他任务依然有运行的机会。
```
#### diff算法
```
1. 概念：React对树的算法进行了简洁的优化，由于DOM节点操作涉及到跨层级的移动操作少到可以忽略不计，所以React只对树进行分层比较。当发现节点已经不存在时，会删除该节点及所有子节点，不回再做多余的遍历比较，只需要对树进行依次比较即可。
```
#### diff原理
```
- 把树形结构按照层级分解，只⽐较同级元素。 给列表结构的每个单元添加唯⼀的key 属性，⽅便⽐较。 React 只会匹配相同 组件名 的 component 合并操作，调⽤ component 的 setState ⽅法的时候, React将其标记为 dirty。到每⼀个事件循环结束, React 检查所有标记 dirty 的 component重新绘制. 选择性⼦树渲染。开发⼈员可以重写 shouldComponentUpdate 提⾼ diff的性能。
```
#### 虚拟DOM的工作原理
```
- Virtual DOM 是⼀个轻量级的 JavaScript 对象，它最初只是 真实DOM 的副本。它是⼀个节点树，它将元素、它们的属性和内容作为对象及其属性。 React 的渲染函数从 React 组件中创建⼀个节点树。然后它响应数据模型中的变化来更新该树，该变化是由⽤户或系统完成的各种动作引起的。
- 渲染步骤：
    1. 每当底层数据发⽣改变时，整个 UI 都将在 Virtual DOM 描述中重新渲染
    2. 然后计算之前 DOM 结构与结构的之间的差异
    3. 完成计算后，将只⽤实际更改的内容更新 真实DOM。
```
#### 为什么虚拟 dom 会提⾼性能
```
-  虚拟 dom 相当于在 js 和真实 dom 中间加了⼀个缓存，利⽤ dom diff 算法避免了没有必要的 dom 操作，从⽽提⾼性能。⽤ JavaScript 对象结构表示 DOM 树的结构；然后⽤这个树构建⼀个真正的 DOM 树，插入到⽂档当中当状态变更的时候，重新构造⼀棵新的对象树。然后⽤新的树和旧的树进⾏⽐较，记录两棵树差异，把 所记录的差异应⽤到真正的 DOM 树上，视图就更新了。
```
#### React 的虚拟DOM是怎么实现的
```
- 首先说说为什么要使用Virturl DOM，因为操作真实DOM的耗费的性能代价太高，所以react内部使用js实现了一套dom结构，在每次操作在和真实dom之前，使用实现好的diff算法，对虚拟dom进行比较，递归找出有变化的dom节点，然后对其进行更新操作。为了实现虚拟DOM，我们需要把每一种节点类型抽象成对象，每一种节点类型有自己的属性，也就是prop，每次进行diff的时候，react会先比较该节点类型，假如节点类型不一样，那么react会直接删除该节点，然后直接创建新的节点插入到其中，假如节点类型一样，那么会比较prop是否有更新，假如有prop不一样，那么react会判定该节点有更新，那么重渲染该节点，然后在对其子节点进行比较，一层一层往下，直到没有子节点
```
#### 什么是JSX
```
- JSX 是JavaScript XML的简写。是一种JavaScript的语法扩展，运用于React架构中，其格式比较像是模版语言，但事实上完全是在JavaScript内部实现的。元素是构成React应用的最小单位，JSX就是用来声明React当中的元素，React使用JSX来描述用户界面。
```
#### 为什么代码中一定要引入React
```
- JSX只是为 React.createElement(component,props,...children)方法提供的语法糖。
所有的 JSX代码最后都会转换成 React.createElement(...)， Babel帮助我们完成了这个转换的过程。所以使用了 JSX的代码都必须引入 React。
```
#### 理解一切皆为组件
```
- 组件是 React 应⽤ UI 的构建块。这些组件将整个 UI 分成⼩的独⽴并可重⽤的部分。每个组件彼此独⽴，⽽不会影响 UI 的其余部分。
```
#### 生命周期
```
1. 阶段：
    * 初始渲染阶段：组件准备设置初始化状态和默认属性。
    * 挂载阶段：react 组件已经准备好挂载到浏览器 DOM 中。componentWillMount -> render -> componentDidMount
    * 更新阶段：它只有在props或状态发⽣变化时才可能更新和重新渲染。componentWillReceiveProps -> shouldComponentUpdate -> componentWillUpdate -> componentDidUpdate
    * 卸载阶段：组件卸载或销毁。componentWillUnmount
    * 错误处理阶段：不论在渲染的过程中，还是在生命周期方法中或是在任何子组件的构造函数中发生错误，该组件都会被调用。componentDidCatch
```
2. 钩子函数：
    1. <b style="color:#FFA500">componentWillMount()</b>:在render()方法之前执行，可以在这里初始化状态，在这个方法中setState不会发生重新渲染(re-render)。这是服务端渲染(server render)中唯一调用的钩子(hook)。
    2. <b style="color:#FFA500">componentDidMount()</b>： 这个方法会在render()之后立即执行，在这个方法中可以操作真实DOM，加载服务器数据，使用setState()方法触发重新渲染(re-render)。
    3. <b style="color:#FFA500">componentWillReceiveProps(nextProps)</b>：在已经挂载的组件(mounted component)接收到新props时触发。在props发生变化(或者说新传入的props)来更新state，需要比较this.props和nextProps, 然后使用this.setState()方法来改变this.state。
    4. <b style="color:#FFA500">shouldComponentUpdate(nextProps,nextState)</b>:在接收到新props或state时，或者说在componentWillReceiveProps(nextProps)后触发。确定是否发生重新渲染，默认情况返回true，表示会发生重新渲染。这个方法在首次渲染时或者forceUpdate()时不会触发。
    5. <b style="color:#FFA500">componentWillUpdate(nextProps, nextState)</b>：在props或state发生改变或者shouldComponentUpdate(nextProps, nextState)触发后, 在render()之前执行。在组件初始化时不会调用。不能在这个函数中调用this.setState()方法。如果shouldComponentUpdate(nextProps, nextState)返回false，那么componentWillUpdate()不会被触发。
    6. <b style="color:#FFA500">componentDidUpdate(prevProps, prevState)</b>:在发生更新或componentWillUpdate(nextProps, nextState)后执行。这个方法可以对组件中的DOM进行操作。
    7. <b style="color:#FFA500">componentWillUnmount()</b>:在组件卸载(unmounted)或销毁(destroyed)之前触发。这个方法可以让你处理一些必要的清理操作，比如无效的timers、interval，或者取消网络请求，或者清理任何在componentDidMount()中创建的DOM元素(elements)。
#### Refs的作用
```
- Refs 是 React 提供给我们的安全访问 DOM元素或者某个组件实例的句柄。可以为元素添加ref属性然后在回调函数中接受该元素在 DOM 树中的句柄，该值会作为回调函数的第一个参数返回。
```
#### key的作用
```
- key ⽤于识别唯⼀的 Virtual DOM 元素及其驱动 UI 的相应数据。它们通过回收DOM 中当前所有的元素来帮助 React 优化渲染。这些 key 必须是唯⼀的数字或字符串，React 只是重新排序元素⽽不是重新渲染它们。这可以提⾼应⽤程序的性能。
- 在开发过程中，我们需要保证某个元素的 key 在其同级元素中具有唯一性。在 React Diff 算法中React 会借助元素的 Key 值来判断该元素是新近创建的还是被移动而来的元素，从而减少不必要的元素重渲染。此外，React 还需要借助 Key 值来判断元素与本地状态的关联关系，因此我们绝不可忽视转换函数中 Key 的重要性。
```
#### Redux
- <b>为什么要用redux</b>
```
    * 在React中，数据在组件中是单向流动的，数据从一个方向父组件流向子组件（通过props）,所以，两个非父子组件之间通信就相对麻烦，redux的出现就是为了解决state里面的数据问题。
```
- <b style="color:skyblue">三个原则</b>
```
    1. 唯一数据源：整个应⽤的状态存储在单个 store 中的对象/状态树⾥。单⼀状态树可以更容易地跟踪随时间的变化，并调试或检查应⽤程序。
    2. 保持只读状态：改变状态的唯⼀⽅法是去触发⼀个动作。动作是描述变化的普通 JS 对象。就像 state 是数据的最⼩表示⼀样，该操作是对数据更改的最⼩表示。
    3.数据改变只能通过纯函数来执行：为了指定状态树如何通过操作进⾏转换，你需要纯函数。纯函数是那些返回值仅取决于其参数值的函数。
```
- <b style="color:skyblue">唯一数据源理解</b>
```
    Redux 使⽤ “Store” 将程序的整个状态存储在同⼀个地⽅。因此所有组件的状态都存储在Store 中，并且它们从 Store 本身接收更新。单⼀状态树可以更容易地跟踪随时间的变化，并调试或检查程序。
```
- <b style="color:skyblue">Reducer的作用</b>
```
    Reducers 是纯函数，它规定应⽤程序的状态怎样因响应 ACTION ⽽改变。Reducers 通过接受先前的状态和 action 来⼯作，然后它返回⼀个新的状态。它根据操作的类型确定需要执⾏哪种更新，然后返回新的值。如果不需要完成任务，它会返回原来的状态。
```
- <b style="color:skyblue">store在Redux中的意义</b>
```
    Store 是⼀个 JavaScript 对象，它可以保存程序的状态，并提供⼀些⽅法来访问状态、调度操作和注册侦听器。应⽤程序的整个状态/对象树保存在单⼀存储中。因此，Redux ⾮常简单且是可预测的。我们可以将中间件传递到 store 来处理数据，并记录改变存储状态的各种操作。所有操作都通过 reducer 返回⼀个新状态。
```
#### 了解redux么说⼀下redux吧
```
- redux 是⼀个应⽤数据流框架，主要是解决了组件间状态共享的问题，原理是集中式管理，主要有三个核⼼⽅法，action，store，reducer，⼯作流程是 view 调⽤store 的 dispatch 接收 action 传⼊ store，reducer 进⾏ state 操作，view 通过store 提供的 getState 获取最新的数据，flux 也是⽤来进⾏数据操作的，有四个组成部分 action，dispatch，view，store，⼯作流程是 view 发出⼀个 action，派发器接收 action，让 store 进⾏数据更新，更新完成以后 store 发出 change，view接受 change 更新视图。Redux 和 Flux 很像。主要区别在于 Flux 有多个可以改变应⽤状态的 store，在 Flux 中 dispatcher 被⽤来传递数据到注册的回调事件，但是在 redux 中只能定义⼀个可更新状态的 store，redux 把 store 和 Dispatcher 合并,结构更加简单清晰 新增 state,对状态的管理更加明确，通过 redux，流程更加规范了，减少⼿动编码量，提⾼了编码效率，同时缺点时当数据更新时有时候组件不需要，但是也要重新绘制，有些影响效率。⼀般情况下，我们在构建多交互，多数据流的复杂项⽬应⽤时才会使⽤它们。
```

#### router
```
1.什么是react-router？
    React Router 是一个基于 React 之上的强大路由库，可以快速地向应用添加视图和数据流，同时保持 UI 与 URL 同步。


2.React Router 与 history 库的区别?
    React Router 是history库的包装器，它处理浏览器的window.history与浏览器和哈希历史的交互。它还提供了内存历史记录，这对于没有全局历史记录的环境非常有用，例如移动应用程序开发（React Native）和使用 Node 进行单元测试。


3.history 中的 push() 和 replace() 方法的目的是什么?
    一个 history 实例有两种导航方法：push()和replace()
    如果将 history 视为一个访问位置的数组，则push()将向数组添加一个新位置，replace()将用新的位置替换数组中的当前位置。
    

4.编程式导航
    所有的被HashRouter等路由渲染的后代组件的props中都有一个路由信息对象history，其中有一个方法push就是用来切换路由的，参数接受一个路由path
this.props.history.push('/home') //构造函数constructor中则是第一个参数props


5.NavLink组件
    NavLink 和 Link 的作用一样，只不过当前导航激活时（NavLink 的 to 和页面 url 中的路径相同时导航被激活）会给当前被激活的 NavLink 添加一个 active 类名；如果设置 高亮当前激活的导航 给 active 类名添加样式就可以了


6.Link组件
    是 react-router-dom的内置组件 起作用和VueRouter 和 router-link 类似 点击它可以跳转到指定路由
使用时需要导入 可以为其设置一个to属性 值就是单机这个Link时要跳转到路由的path（link 最后会被渲染成a标签展示出来）
因此在开发时尽量少些a 标签 因为路由不仅有 hash 模式还是 history 模式；写 Link 它会自动根据模式切换路径
且to的值的这个路由path必须在Route 中注册过才行（只要在应用中注册过即可）


7.switch组件
    Switch组件 使用时需导入 当Route匹配一个路由后就不在往后匹配 使用该组件


8.受保护的路由
    在真实的项目中，我们会对一些路由进行保护机制，像有些页面用户没有登录则不允许访问。vueRouter中有导航守卫来处理这个问题，而在react-router中则需要写受保护的路由来实现  受保护的路由其实说白了就是我们自己实现一个组件来包裹Route组件，然后使用我们自己的组件替换掉Route组件，我们在我们自己的组件中做逻辑判断

9.如何实现默认页面或 404 页面?
    <Switch>呈现匹配的第一个孩子<Route>。 没有路径的<Route>总是匹配。所以你只需要简单地删除 path 属性


10.登录后如何执行自动重定向?
    react-router包在 React Router 中提供了<Redirect>组件。渲染<Redirect>将导航到新位置。与服务器端重定向一样，新位置将覆盖历史堆栈中的当前位置。

```

### react router 的实现
```
    BrowserRouter 或 HashRouter 用来渲染Router所代表的组件
    BrowserRouter --浏览器路由(属于后端路由) 会有一个#，通过这个# HTML 5 History进行前端跳转他的感觉像锚点
    HasRouter --前端has路由（属于前端路由）很简洁没有#，但是需要 server 端支持
    Route 用来匹配组件路径并且筛选需要渲染的组件
    Switch 用来筛选需要渲染的唯一组件
    Link 直接渲染某个页面组件
    Redirect 类似于Link，在没有Route匹配成功时触发
```
#### 什么是react-router
```
React Router 是一个基于 React 之上的强大路由库，可以帮助您快速地向应用添加视图和数据流，同时保持 UI 与 URL 同步。
```
#### react-router与history库的区别
```
React Router 是`history`库的包装器，它处理浏览器的`window.history`与浏览器和哈希历史的交互。它还提供了内存历史记录，这对于没有全局历史记录的环境非常有用，例如移动应用程序开发（React Native）和使用 Node 进行单元测试。
```
#### React 路由是干什么的
```
    根据不同的 url 地址展示不同的内容或页面。
    单页面应用最大的特点就是只有一个 web 页面。因而所有的页面跳转都需要通过javascript实现。当需要根据用户操作展示不同的页面时，我们就需要根据访问路径使用js控制页面展示内容。
```
#### React Link组件
```
    to：可以是一个字符串表示目标路径，也可以是一个对象，包含四个属性：
        pathname:表示指向的目标路径
        search: 传递的搜索参数
        hash:路径的hash值
        state: 地址状态

    replace：是否替换整个历史栈

    innerRef：访问部件的底层引用

```
#### React Router组件
```
    React-router 中最重要的组件，最主要的职责就是根据匹配的路径渲染指定的组件。
    主要属性:

        path：需要匹配的路径

        component：需要渲染的组件

        render：渲染组件的函数

        children ：渲染组件的函数，常用在path无法匹配时呈现的’空’状态即所谓的默认显示状态

```

#### React 路由鉴权 权限控制 
```
    为什么用：  在项目中，我们是希望根据登录人来看下这个人是不是有权限进入当前页面。虽然服务端做了进行接口的权限，但是每一个路由加载的时候都要去请求这个接口太浪费了。所以有时候是通过SESSIONID来校验登陆权限的。

    如何实现：  我们会先把路由表配置抽离成一个文件，路由表一般为一个数组，数组中存放保存有路由信息的对象。这个对象的属性常有路径和这个路径对应加载的组件，以及一个鉴别权限的属性，大多用来判断用户是否登录。再封装一个高阶组件用map来遍历渲染Router组件，在map遍历时做判断，如果没有权限查看当前页面的情况，一般来讲有两种处理方式，一是直接重定向到另一个页面（如首页），二是渲染一个无权限页面，提示用户因为没有当前页面的权限所以无法查看。
    在最终的路由中，我们会优先匹配无需鉴权的页面路径，保证所有用户在访问无需鉴权的页面时，第一时间就可以看到页面。然后再去匹配需要鉴权的页面路径，最终如果所有的路径都匹配不到的话，再渲染 404 页面告知用户当前页面路径不存在。

```
#### HashRouter(hashrouter) 与 BrowserRouter(browserrouter)的区别
```
    从原理上：
        HashRouter在路径中包含了#，相当于HTML的锚点定位。
        BrowserRouter使用的是HTML5的新特性History，没有HashRouter(锚点定位)那样通用，低版本浏览器可能不支持。
    从用法上：
        BrowserRouter进行组件跳转时可以传递任意参数实现组件间的通信，而HashRouter不能(除非手动拼接URL字符串)，因此一般配合Redux使用，实现组件间的数据通信。

    HashRouter
        1. HashRouter相当于锚点定位，因此不论#后面的路径怎么变化，请求的都相当于是#之前的那个页面。可以很容易的进行前后端不分离的部署(也就是把前端打包后的文件放到服务器端的public或static里)。
    BrowserRouter
        1. BrowserRouter模式下请求的链接都是ip地址:端口/xxxx/xxxx，因此相当于每个URL都会访问一个不同的后端地址，如果后端没有覆盖到路由就会产生404错误。
```

#### 


#### 展示组件和容器组件之间有何不同
```
- 展示组件关⼼组件看起来是什么。展示专⻔通过 props 接受数据和回调，并且⼏乎不会有⾃身的状态，但当展示组件拥有⾃身的状态时，通常也只关⼼ UI 状态⽽不是数据的状态。 容器组件则更关⼼组件是如何运作的。容器组件会为展示组件或者其它容器组件提供数据和⾏为(behavior)，它们会调⽤ Flux actions，并将其作为回调提供给展示组件。容器组件经常是有状态的，因为它们是(其它组件的)数据源。
```
#### 类组件和函数式组件之间有何不同
```
- 类组件不仅允许你使⽤更多额外的功能，如组件⾃身的状态和⽣命周期钩⼦，也能使组件直接访问 store 并维持状态 当组件仅是接收 props，并将组件⾃身渲染到⻚⾯时，该组件就是⼀个 '⽆状态组件(stateless component)'，可以使⽤⼀个纯函数来创建这样的组件。这种组件也被称为哑组件(dumb components)或展示组件。而且函数组件的性能比类组件的性能要高，因为类组件使用的时候要实例化，而函数组件直接执行函数取返回结果即可。为了提高性能，尽量使用函数组件。
```
#### (组件的)状态(state)和属性(props)之间有何不同
```
- State 是⼀种数据结构，⽤于组件挂载时所需数据的默认值。State 可能会随着时间的推移⽽发⽣突变，但多数时候是作为⽤户事件⾏为的结果。 Props(properties 的简写)则是组件的配置。props 由⽗组件传递给⼦组件，并且就⼦组件⽽⾔，props是不可变的(immutable)。组件不能改变⾃身的 props，但是可以把其⼦组件的props 放在⼀起(统⼀管理)。Props 也不仅仅是数据--回调函数也可以通过 props 传递。
```
#### 何为受控组件
```
- 在HTML中，类似input的表单元素会维护⾃身的状态，并基于⽤户的输⼊来更新。当⽤户提交表单时，前⾯提到的元素的值将随表单⼀起被发送。但在 React 中会有些不同，包含表单元素的组件将会在 state 中追踪输⼊的值，并且每次调⽤回调函数时，如 onChange 会更新 state，重新渲染组件。⼀个输⼊表单元素，它的值通过 React 的这种⽅式来控制，这样的元素就被称为"受控元素"。
```
#### 受控组件和非受控组件区别是啥
```
- 受控组件是 React 控制中的组件，并且是表单数据真实的唯一来源。
- 非受控组件是由 DOM 处理表单数据的地方，而不是在 React 组件中。
```
#### 何为⾼阶组件
```
- ⾼阶组件是重⽤组件逻辑的⾼级⽅法，是⼀种源于 React 的组件模式。 ⾼阶组件是⼀个以组件为参数并返回⼀个新组件的函数。HOC 允许你重⽤代码、逻辑和引导抽象。最常⻅的可能是 Redux 的 connect 函数。除了简单分享⼯具库和简单的组合，HOC 最好的⽅式是共享 React 组件之间的⾏为。如果你发现你在不同的地⽅写了⼤量代码来做同⼀件事时，就应该考虑将代码重构为可重⽤的 HOC。
```
#### 在生命周期中的哪一步你应该发起 AJAX 请求
```
我们应当将AJAX 请求放到 componentDidMount 函数中执行，主要原因有下：
- React Fiber 会通过开始或停止渲染的方式优化应用性能，其会影响到 componentWillMount 的触发次数。对于 componentWillMount 这个生命周期函数的调用次数会变得不确定，React 可能会多次频繁调用 componentWillMount。如果我们将 AJAX 请求放到 componentWillMount 函数中，那么显而易见其会被触发多次，自然也就不是好的选择。
- 如果我们将AJAX 请求放置在生命周期的其他函数中，我们并不能保证请求仅在组件挂载完毕后才会要求响应。如果我们的数据请求在组件挂载之前就完成，并且调用了setState函数将数据添加到组件状态中，对于未挂载的组件则会报错。而在 componentDidMount 函数中进行 AJAX 请求则能有效避免这个问题。
```
#### 描述事件在 React 中的处理⽅式
```
- 为了解决跨浏览器兼容性问题，React 会将浏览器原生事件（Browser Native Event）封装为合成事件（SyntheticEvent）传入设置的事件处理器中。这里的合成事件提供了与原生事件相同的接口，不过它们屏蔽了底层浏览器的细节差异，保证了行为的一致性。另外有意思的是，React 并没有直接将事件附着到子元素上，而是以单一事件监听器的方式将所有的事件发送到顶层进行处理。这样 React 在更新 DOM 的时候就不需要考虑如何去处理附着在 DOM 上的事件监听器，最终达到优化性能的目的。
```
#### 原生事件和React事件的区别
```
- React 事件使用驼峰命名，而不是全部小写
- 通过 JSX , 你传递一个函数作为事件处理程序，而不是一个字符串。
- 在 React 中你不能通过返回 false 来阻止默认行为。必须明确调用 preventDefault。
```
#### 在构造函数调用 super 并将 props 作为参数传入的作用是啥
```
- 在调用 super() 方法之前，子类构造函数无法使用this引用，ES6 子类也是如此。将 props 参数传递给 super() 调用的主要原因是在子构造函数中能够通过this.props来获取传入的 props。
```

#### 什么是 React Hooks
```
- Hooks是 React 16.8 中的新添加内容。它们允许在不编写类的情况下使用state和其他 React 特性。使用 Hooks，可以从组件中提取有状态逻辑，这样就可以独立地测试和重用它。Hooks 允许咱们在不改变组件层次结构的情况下重用有状态逻辑，这样在许多组件之间或与社区共享 Hooks 变得很容易。
```

#### 使用 React Hooks 好处是啥
```
- Hooks 通常支持提取和重用跨多个组件通用的有状态逻辑，而无需承担高阶组件或渲染 props 的负担。Hooks 可以轻松地操作函数组件的状态，而不需要将它们转换为类组件。Hooks 在类中不起作用，通过使用它们，咱们可以完全避免使用生命周期方法，例如 componentDidMount，componentDidUpdate、componentWillUnmount。相反，使用像useEffect这样的内置钩子。
- 跨组件复用: 其实 render props / HOC 也是为了复用，相比于它们，Hooks 作为官方的底层 API，最为轻量，而且改造成本小，不会影响原来的组件层次结构和传说中的嵌套地狱。
- 类定义更为复杂
    1. 不同的生命周期会使逻辑变得分散且混乱，不易维护和管理
    2. 时刻需要关注this的指向问题
    3. 代码复用代价高，高阶组件的使用经常会使整个组件树变得臃肿
- 状态与UI隔离: 正是由于 Hooks 的特性，状态逻辑会变成更小的粒度，并且极容易被抽象成一个自定义 Hooks，组件中的状态和 UI 变得更为清晰和隔离。
```

#### 内置Hooks(钩子函数)
```
- 状态钩子 (useState): 用于定义组件的 State，其到类定义中this.state的功能
- 生命周期钩子 (useEffect):类定义中有许多生命周期函数，而在 React Hooks 中也提供了一个相应的函数 (useEffect)，这里可以看做componentDidMount、componentDidUpdate和componentWillUnmount的结合。
- useContext：获取context对象
- useReducer：类似于 Redux 思想的实现，但其并不足以替代 Redux，可以理解成一个组件内部的 redux
- useCallback：缓存回调函数，避免传入的回调每次都是新的函数实例而导致依赖组件重新渲染，具有性能优化的效果。
- useMemo：用于缓存传入的 props，避免依赖的组件每次都重新渲染。
- useRef：获取组件的真实节点
```
#### React 中的StrictMode(严格模式)是什么
```
- React 的StrictMode是一种辅助组件，可以帮助咱们编写更好的 react 组件，可以使用<StrictMode />包装一组组件，并且可以帮咱们以下检查：
    * 验证内部组件是否遵循某些推荐做法，如果没有，会在控制台给出警告。
    * 验证是否使用的已经废弃的方法，如果有，会在控制台给出警告。
    * 通过识别潜在的风险预防一些副作用。
```
#### 为什么类方法需要绑定到类实例
```
- 在 JS 中，this 值会根据当前上下文变化。在 React 类组件方法中，开发人员通常希望 this 引用组件的当前实例，因此有必要将这些方法绑定到实例。
```
#### 描述MVC
```
- 传统的 MVC 模式在分离数据(Model)、UI(View和逻辑(Controller)方面工作得很好，但是 MVC 架构经常遇到两个主要问题:
    * 数据流不够清晰:跨视图发生的级联更新常常会导致混乱的事件网络，难于调试。
    * 缺乏数据完整性:模型数据可以在任何地方发生突变，从而在整个UI中产生不可预测的结果。
```
#### 什么是 React Context
```
- Context 通过组件树提供了一个传递数据的方法，从而避免了在每一个层级手动的传递 props 属性。
```
#### 如何避免组件的重新渲染
```
- React 中最常见的问题之一是组件不必要地重新渲染。React 提供了两个方法，在这些情况下非常有用：
    * React.memo():这可以防止不必要地重新渲染函数组件
    * PureComponent:这可以防止不必要地重新渲染类组件
- 这两种方法都依赖于对传递给组件的props的浅比较，如果 props 没有改变，那么组件将不会重新渲染。虽然这两种工具都非常有用，但是浅比较会带来额外的性能损失，因此如果使用不当，这两种方法都会对性能产生负面影响。
```
#### 什么是纯函数
```
- 纯函数是不依赖并且不会在其作用域之外修改变量状态的函数。本质上，纯函数始终在给定相同参数的情况下返回相同结果。
```
#### 为什么不直接更新 state 呢
```
- 如果试图直接更新 state ，则不会重新渲染组件。需要使用setState()方法来更新 state。它调度对组件state对象的更新。当state改变时，组件通过重新渲染来响应。
```
#### 调用setState之后发生了什么
```
-  在代码中调⽤ setState 函数之后，React 会将传⼊的参数对象与组件当前的状态合并，然后触发所谓的调和过程（Reconciliation）。经过调和过程，React 会以相对⾼效的⽅式根据新的状态构建 React 元素树并且着⼿重新渲染整个 UI 界⾯。在React 得到元素树之后，React 会⾃动计算出新的树与⽼树的节点差异，然后根据差异对界⾯进⾏最⼩化重渲染。在差异计算算法中，React 能够相对精确地知道哪些位置发⽣了改变以及应该如何改变，这就保证了按需更新，⽽不是全部重新渲染。
```
#### 当调用setState时，React render 是如何工作的
```
- 虚拟 DOM 渲染:当render方法被调用时，它返回一个新的组件的虚拟 DOM 结构。当调用setState()时，render会被再次调用，因为默认情况下shouldComponentUpdate总是返回true，所以默认情况下 React 是没有优化的。
- 原生 DOM 渲染:React 只会在虚拟DOM中修改真实DOM节点，而且修改的次数非常少——这是很棒的React特性，它优化了真实DOM的变化，使React变得更快。
```
#### setState到底是异步还是同步
```
- setState只在合成事件和钩子函数中是“异步”的，在原生事件和setTimeout 中都是同步的。
- setState 的“异步”并不是说内部由异步代码实现，其实本身执行的过程和代码都是同步的，只是合成事件和钩子函数的调用顺序在更新之前，导致在合成事件和钩子函数中没法立马拿到更新后的值，形成了所谓的“异步”，当然可以通过第二个参数setState(partialState, callback)中的callback拿到更新后的结果。
- setState 的批量更新优化也是建立在“异步”（合成事件、钩子函数）之上的，在原生事件和setTimeout 中不会批量更新，在“异步”中如果对同一个值进行多次setState，setState的批量更新策略会对其进行覆盖，取最后一次的执行，如果是同时setState多个不同的值，在更新时会对其进行合并批量更新。
```
#### 为什么有时连续多次setState只有一次生效
```
- react为了提高整体的渲染性能，会将一次渲染周期中的state进行合并，在这个渲染周期中你对所有setState的所有调用都会被合并起来之后，再一次性的渲染，这样可以避免频繁的调用setState导致频繁的操作dom，提高渲染性能。具体的实现方面，可以简单的理解为react中存在一个状态变量isBatchingUpdates，当处于渲染周期开始时，这个变量会被设置成true，渲染周期结束时，会被设置成false，react会根据这个状态变量，当出在渲染周期中时，仅仅只是将当前的改变缓存起来，等到渲染周期结束时，再一次性的全部render。
```
#### shouldComponentUpdate 的作用
```
- shouldComponentUpdate 允许我们手动地判断是否要进行组件更新，根据组件的应用场景设置函数的合理返回值能够帮我们避免不必要的更新。
```
#### React实现的移动应用中，如果出现卡顿，有哪些可以考虑的优化方案
```
- 增加shouldComponentUpdate钩子对新旧props进行比较，如果值相同则阻止更新，避免不必要的渲染，或者使用PureReactComponent替代Component，其内部已经封装了shouldComponentUpdate的浅比较逻辑。
- 对于列表或其他结构相同的节点，为其中的每一项增加唯一key属性，以方便React的diff算法中对该节点的复用，减少节点的创建和删除操作。
- render函数中减少类似onClick={() => {doSomething()}}的写法，每次调用render函数时均会创建一个新的函数，即使内容没有发生任何变化，也会导致节点没必要的重渲染，建议将函数保存在组件的成员对象中，这样只会创建一次。
- 组件的props如果需要经过一系列运算后才能拿到最终结果，则可以考虑使用reselect库对结果进行缓存，如果props值未发生变化，则结果直接从缓存中拿，避免高昂的运算代价
- webpack-bundle-analyzer分析当前页面的依赖包，是否存在不合理性，如果存在，找到优化点并进行优化。
```
#### 组件渲染流程
```
- 使用 React.createElement或 JSX编写 React组件，实际上所有的 JSX代码最后都会转换成 React.createElement(...)， Babel帮助我们完成了这个转换的过程。
- createElement函数对 key和 ref等特殊的 props进行处理，并获取 defaultProps对默认 props进行赋值，并且对传入的孩子节点进行处理，最终构造成一个 ReactElement对象（所谓的虚拟 DOM）。
- ReactDOM.render将生成好的虚拟 DOM渲染到指定容器上，其中采用了批处理、事务等机制并且对特定浏览器进行了性能优化，最终转换为真实 DOM。
```
#### redux-thunk和redux-saga区别
```
    redux-thunk在action中处理异步等副作用操作，此时的action是一个函数，以dispatch，getState作为形参，函数体内的部分可以执行异步。在redux-saga中，action是plain object（原始对象），并且集中处理了所有的异步操作。redux-saga是通过ES6中的generator实现的（babel的基础版本不包含generator语法，因此需要在使用saga的地方import ‘babel-polyfill’）。redux-saga本质是一个可以自执行的generator。
```
#### 纯组件purecomponent
```
    React.PureComponent 与 React.Component 很相似。两者的区别在于 React.Component 并未实现 shouldComponentUpdate()，而 React.PureComponent 中以浅层对比 prop 和 state 的方式来实现了该函数。
```
#### react susponce+lazy (懒加载)
```
    <Suspense> 组件，让你可以“等待”目标代码加载，并且可以直接指定一个加载的界面，让它在用户等待的时候显示。
```

#### immutable
```
什么场景下使用？
有时候reducer中需要使用深拷贝，但是自己写会有些缺陷，比如说不能有undefined。这时候使用Immutable库就可以实现性能优化。每次修改一个 Immutable 对象时都会创建一个新的不可变的对象，在新对象上操作并不会影响到原对象的数据。immutable常用的类型有：Map用于操作对象，List用于操作数组。

安装：
cnpm i --save immmutable

实现原理：
Immutable实现的原理是 Persistent Data Structure（持久化数据结构），也就是使用旧数据创建新数据时，要保证旧数据同时可用且不变。同时为了避免深拷贝把所有节点都复制一遍带来的性能损耗，Immutable 使用 了 Structural Sharing（结构共享），即如果对象树中一个节点发生变化，只修改 这个节点和受它影响的父节点，其它节点则进行共享。
```

#### 虚拟滚动方案
```
什么场景下
后端给我们的数据远大于我们需要展示的数据的量，但是我们只需要展示一定数量的数据，其他本次不需要显示的数据就不渲染出来，数据拿到了但是我们不渲染
```
#### 小程序taro技术遇到的坑
```
    错误：通过git或svn，拉取的项目，一定要和拉取项目的node版本和taro版本都保持一致，否则就会报错，运行失败
    解决：我当时因为版本不一致报错的情况，报的错也没说版本问题，网上找了一通，后来还是试着统一版本就好了，当时真的是想哭。

    编译dist文件经常有一些第三方的错，要不就是某个方法不存在，这种问题我一般就把微信开发者工具关了（这个工具也是有很多bug）然后把taro编译的dist文件夹（主意只有dist文件夹）删掉，然后重新执行npm run dev:weapp之后这个问题就好了，虽然不知道原理，但是能解决问题，主要是不会耽误我们的时间

```
#### axios技术的请求拦截和响应拦截
```
    作用：
        1. 拦截器可以用来对敏感信息进行处理，不管是请求发送前，还是响应结果之后。
        2. 在发起的所有请求在请求头中添加信息,当后端接口需要在请求当中携带token 的时候，我们每次发起请求都要写一遍请求头 headers 这里就可以通过请求拦截器设置信息
        3. 在不需要取得所有的响应数据，只取得需要的数据，比如通过相应的状态属性返回对应的数据，就会添加响应拦截器
```
#### 什么是dva
```
    1. dva 首先是一个基于 redux 和 redux-saga 的数据流方案，然后为了简化开发体验，dva 还额外内置了 react-router 和 fetch，所以也可以理解为一个轻量级的应用框架。
    2. 每当你使用React的时候都需要引入很多的模块，那么dva就是把这些用到的模块集成在一起，形成一定的架构规范。把react常常需要我们必须写的需要用到的引用、代码都集成在了一起，比如一些依赖、必写的一些ReactDOM.render、引入saga、redux控制台工具、provider包裹等都省去不写，大大提高我们的开发效率
    3. 增加了一个 Subscriptions, 用于收集其他来源的 action, eg: 键盘操作、滚动条、websocket、路由等
    4. 在react-redux上开发的dva+在redux-saga基础上开发的dva-core+在webpack基础上开发的roadhog进行打包启动服务
    5. 数据流向（基于redux，所以同react-redux）
    6. 输入url渲染对应的组件，该组件通过dispatch去出发action里面的函数，如果是同步的就去进入model的ruducer去修改state，如果是异步比如fetch获取数据就会被effect拦截通过server交互获取数据进而修改state，同样state通过connect将model、状态数据与组件相连

```
#### dva数据流向
```
    数据流向：数据的改变发生通常是通过用户交互行为或者浏览器行为（如路由跳转等）触发的，当此类行为会改变数据的时候可以通过 dispatch 发起一个 action，如果是同步行为会直接通过 Reducers 改变 State ，如果是异步行为（副作用）会先触发 Effects 然后流向 Reducers 最终改变 State。

```
#### 组件通信
```
    1. 父组件向子组件通信
        父组件通过向子组件传递 props，子组件得到 props 后进行相应的处理。
    2. 子组件向父组件通信
        利用回调函数，可以实现子组件向父组件通信：父组件将一个函数作为 props 传递给子组件，子组件调用该回调函数，便可以向父组件通信。
    3. 跨级组件通信
        所谓跨级组件通信，就是父组件向子组件的子组件通信，向更深层的子组件通信。跨级组件通信可以采用下面两种方式：

            1. 中间组件层层传递 props
            2. 使用 context 对象

        对于第一种方式，如果父组件结构较深，那么中间的每一层组件都要去传递 props，增加了复杂度，并且这些 props 并不是这些中间组件自己所需要的。不过这种方式也是可行的，当组件层次在三层以内可以采用这种方式，当组件嵌套过深时，采用这种方式就需要斟酌了。
        使用 context 是另一种可行的方式，context 相当于一个全局变量，是一个大容器，我们可以把要通信的内容放在这个容器中，这样一来，不管嵌套有多深，都可以随意取用。使用 context 也很简单，需要满足两个条件：
            1. 上级组件要声明自己支持 context，并提供一个函数来返回相应的 context 对象
            2. 子组件要声明自己需要使用 context
    4.非嵌套组件间通信
        非嵌套组件，就是没有任何包含关系的组件，包括兄弟组件以及不在同一个父级中的非兄弟组件。对于非嵌套组件，可以采用下面两种方式：
            利用二者共同父组件的 context 对象进行通信
            使用自定义事件的方式
    5.redux

```
#### 手动中断fetch
```
    AbortController 用于手动终止一个或多个DOM请求，通过该对象的AbortSignal注入的Fetch的请求中。AbortController是由dom标准实现的。
```
#### 浏览器中输入一个 URL至页面呈现的过程是什么
```
    1. DNS域名解析
        我们在浏览器输入网址，其实就是要向服务器请求我们想要的页面内容，所有浏览器首先要确认的是域名所对应的服务器在哪里。将域名解析成对应的服务器IP地址这项工作，是由DNS服务器来完成的。客户端收到你输入的域名地址后，它首先去找本地的hosts文件，检查在该文件中是否有相应的域名、IP对应关系，如果有，则向其IP地址发送请求，如果没有，再去找DNS服务器。
    2. 建立TCP连接
        拿到服务器IP了，下一步自然就是链接到该服务器。客户端发送一个带有SYN标志的数据包给服务端，服务端收到后，回传一个带有SYN/ACK标志的数据包以示传达确认信息，最后客户端再回传一个带ACK标志的数据包，代表握手结束，连接成功。
    3. 发送HTTP请求
        与服务器建立了连接后，就可以向服务器发起请求了。 请求行包括请求方法、URI、HTTP版本。首部字段传递重要信息，包括请求首部字段、通用首部字段和实体首部字段。我们可以从报文中看到发出的请求的具体信息。
    4. 服务器处理请求
        服务器端收到请求后的由web服务器（准确说应该是http服务器）处理请求，诸如Apache、Ngnix、IIS等。web服务器解析用户请求，知道了需要调度哪些资源文件，再通过相应的这些资源文件处理用户请求和参数，并调用数据库信息，最后将结果通过web服务器返回给浏览器客户端。
    5. 关闭TCP连接
        为了避免服务器与客户端双方的资源占用和损耗，当双方没有请求或响应传递时，任意一方都可以发起关闭请求。与创建TCP连接的3次握手类似，关闭TCP连接，需要4次握手。
    6. 浏览器解析HTML
        浏览器通过解析HTML，生成DOM树，解析CSS，生成CSS规则树，然后通过DOM树和CSS规则树生成渲染树。
    7. 浏览器布局渲染
        根据渲染树布局，计算CSS样式，即每个节点在页面中的大小和位置等几何信息。HTML默认是流式布局的，CSS和js会打破这种布局，改变DOM的外观样式以及大小和位置。

```
#### 常见的http请求
```
    1. GET
    在浏览器地址栏中输入网址访问资源都是通过GET方式发送HTTP请求
        GET 请求可被缓存
        GET 请求保留在浏览器历史记录中
        GET 请求可被收藏为书签
        GET 请求不应在处理敏感数据时使用
        GET 请求有长度限制,不同浏览器的长度限制不同
        GET 请求只应当用于取回数据
    2. POST
    用于向服务器提交数据，请求的参数要在请求体(body)中发送，可用于表单的提交和异步提交（如ajax），理论上，POST传递的数据量没有限制。
        POST 请求不会被缓存
        POST 请求不会保留在浏览器历史记录中
        POST 不能被收藏为书签
        POST 请求对数据长度没有要求
    由于HTTP协议只规定 POST 提交的数据必须放在消息主体（body）中，并没有规定数据必须使用什么编码方式。前后端交互时编码和解码就变的棘手，服务端通常是根据请求头中的Content-Type字段来获知请求中的消息主体是用何种方式编码，再对body进行解析。
    3. PUT
        与POST方法类似，在RESTful设计规范中，一般POST方法代表新增，PUT方法代表整体更新，选择什么方法主要看接口的要求，PUT请求的参数一样要在HTTP请求的消息主体中发送，默认情况下put请求是无法提交表单数据的。
    4. PATCH
        与PUT方法类似，但PATCH方法通常应用于局部更新。
    5. DELETE
        删除某一个资源，默认情况下DELETE方法在 URL 中附带查询参数，也无法提交表单数据的。

```
#### 代码优化
```
    数组和对象操作避免使用构造函数
    尽量避免使用非必要的全局变量
    合理使用缓存机制
        缓存是提高应用性能的一个常规手段，缓存的方式也有很多，比如说浏览器缓存，数据库缓存等等
    减少循环中的活动
    减少不必要的变量
    原生方法更快
        只要有可能，我们尽量使用原生方法，而不是自己用js去重写业务逻辑。 原生方法是用C或者C++之类的编译型语言写出来的，要比JS快很多。 举个例子： 用switch…case代替一系列复杂的if…else 并按照可能出现的几率最大—>最小的顺序组织逻辑，可以得到进一步的优化
    尽量避免使用闭包


```
### Hooks 需要遵循什么规则?
```
    为了使用 hooks，你需要遵守两个规则：

     1. 仅在顶层的 React 函数调用 hooks。也就是说，你不能在循环、条件或内嵌函数中调用 hooks。这将确保每次组件渲染时都以相同的顺序调用 hooks，并且它会在多个 useState 和 useEffect 调用之间保留 hooks 的状态。
     2. 仅在 React 函数中调用 hooks。例如，你不能在常规的 JavaScript 函数中调用 hooks。

```








