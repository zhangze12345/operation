# 基础概念解释

### 用户旅程

> 用户旅程主要用于帮助运营人员创建复杂的运营流程，通过筛选符合条件的用户，在设置的时间点或者满足触发条件后进入用户旅程，然后基于用户筛选条件或触发事件分流，配置不同的运营策略。可基于实际运营场景在用户旅程里配置多个运营策略，待上线后自动执行，从而实现对不同人群的精细化运营或者对用户进行持续的运营。
>
> 例如，在某次促销活动时，基于用户不同的会员等级，推送不同价格区间的产品，针对不同的价格，推送相应的满减优惠券。

### 旅程节点

> 用户旅程中将用户进行分流并实施不同运营计划的策略，主要分为三种类型，按用户筛选条件分流、按触发事件分流和其他型。
>
> #### 旅程节点-按用户筛选条件分流
>
> 用户旅程中旅程节点的一种，由用户筛选+延时设置+触达消息三部分组成，基于用户的历史行为或用户属性进行分流，满足用户筛选条件的用户进入该旅程节点，可以立即或者延迟一段时间以某个触达通道进行发送。
>
> #### 旅程节点-按触发事件分流
>
> 用户旅程中旅程节点的一种，由触发事件+延时设置+触达消息三部分组成，基于用户的行为实时匹配进行分流，满足触发事件的用户进入该旅程节点，可以立即或者延迟一段时间以某个触达通道进行发送。
>
> #### 旅程节点-其他型
>
> 用户旅程中旅程节点的一种，由延时设置、触达消息两部分组成，用户不满足其他的旅程节点（同一父级旅程节点下）则进入该旅程节点，可以立即或者延迟一段时间以某个触达通道进行发送。

### 定时型-单次

> 用户旅程类型的一种，用于创建单次执行的用户旅程，固定的时间，符合筛选条件的用户进入用户旅程。
>
> 例如，某一次秒杀活动的推送。

### 定时型-重复

> 用户旅程类型的一种，用于创建重复执行的用户旅程，每个周期内固定的一个或多个时间，符合筛选条件的用户进入用户旅程。
>
> 例如，大促活动预热期间每天定时推送。

### 触发型-完成A

> 用户旅程类型的一种，用于创建触发型的用户旅程，当用户完成某个行为后进入用户旅程。
>
> 例如，用户成功注册会员后发送欢迎短信。

### 触发型-完成A未完成B

> 用户旅程类型的一种，用于创建触发型的用户旅程，当用户完成一个行为后的一段时间内未完成另一行为则进入用户旅程。
>
> 例如，用户提交订单30分钟内未完成支付的提醒。

### 触达方式

> 触达用户的方式，例如短信、Webhook等。

### 触达通道

> 提供某种触达用户方式的第三方服务商，例如玄武短信。

### 参与限制

> 对于某些类型的用户旅程计划，如定时型-重复、触发型-完成A、触发型-完成A未完成B，可以允许用户在一定时间段内多次参与当前旅程计划，且可以限制次数，该限制仅对当前计划生效。
>
> 默认不允许用户在活动期间多次参与。

### 勿扰设置

> 设置用户的勿扰时间段以及该时间段内的推送策略。
>
> 该设置仅对当前的用户旅程生效。

### 全局触达设置

> 用于设置用户在一个时间段内收到消息的上限，时间段和消息的上限均可自定义。每种触达方式可添加多条限制，多条限制之间是且的关系。该设置的意义在于避免用户同时收到过多的消息推送而造成过度打扰。
>
> 例如，设置一个用户一天内最多接收1条短信且一个月最多接收15条短信。

### 首要目标

> 用于评估用户旅程中运营策略的效果，设定一定时间内完成某个转化事件则视为完成目标。
>
> 用户旅程效果分析页面显示的目标完成率均为首要目标。

### 次要目标

> 为了多维度的评估运营策略的效果，可以设置次要目标，设定一定时间内完成某个转化事件则视为完成目标。首要目标和次要目标的追踪相互独立。

### Webhook

> 是一个 HTTP 形式的回调接口，用以支持自定义的营销行为。当用户被触发（满足触发条件）时，会去回调请求 webhook 接口，并把该用户的基本信息或其他自定义内容以 json 格式的请求体传递给您自有的服务器，您可以在接口中利用这些信息进行后续的操作，比如，对用户进行消息推送、权益发放等。
>
> 例如，常用的场景：对接自建的优惠券发放平台。

### 自动回复

> 微信运营中的一种消息回复机制，当用户关注公众号或给公众号发送消息时，平台根据预先设置的规则予以自动回复。主要有三种自动回复场景，包括关键词回复、收到消息回复和被关注回复。
>
> #### 关键词回复
>
> 当用户给公众号发送消息时，如果命中了后台配置的关键词规则，则自动回复相应的消息内容。
>
> #### 收到消息回复
>
> 当用户给公众号发送消息时，如果未触发其他的回复规则，则回复该场景下设置的回复内容。
>
> #### 被关注回复
>
> 当用户关注公众号时，自动回复设置的消息内容，可以设置多种类型的回复内容。

### 模板消息

> 按照一定的模板样式发送给用户的消息。微信公众服务号后台提供的一种功能，认证的服务号可以配置后使用。智慧运营平台可同步公众号配置的模板消息，在用户旅程中设置运营策略时使用。
>
> 每个服务号最多可以选择模板库中的25个模板来使用，模板消息运营过程中需遵守《微信模板消息运营规范》，新增、修改、移除模板需要在【微信公众平台】-【模板消息】中对模板进行操作。

### 渠道二维码

> 主要用于微信公众服务号在不同渠道的推广，可以针对不同渠道制定差异化的运营策略，也可以分析不同渠道的推广拉新效果，从而指导下一次的精细化运营。