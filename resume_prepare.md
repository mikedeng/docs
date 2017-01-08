
https://www.youtube.com/watch?v=HWBw7mFTIGY
https://www.youtube.com/watch?v=vF2YACrLP8w

Roles

Agent & Customer
& Manager

+ satisfacation survey

    It used for agent who  ask for satisfacation survey about their own service quality.

+ sortition
  管理员可以批量抓取
    Manager collect random satisfacation survey count, so that he make a score for each of them, let say 7 , 8 out of 10.

After the scoring, it will generate a two demensions statistic chart. like x axis marked by group name and y by average score.

Lastly, the whole evaluation is clearly displayed


+ wechat message

    - Firstly, wechat will push the message from the customer to our callback server with it's url set in the wechat server.

    - Secondly, after receiving the message, I should identify the user by wechat openid. During the communication with the wechat server, I  must reserved the token in redis, because it was limited as 2000 times refreshment each day.

    - Thirdly, check the agent status(online, offline, busy), save and deliver message to the agent.


    也有没有限制请求次数的api, 比如微信服务器的ip服务, 它可以用来检查token是否有效.
    -- They are none limited apis, like wechat server ip service, deliver a token, then it will return ip address.
        the kind of Wechat api can be use as token check.


+ Dispatch customers
    - The administrator make kind of dispatchers, let's say provinces, cities of the customers.
      And set the dispatchers' receiver as a agent or agent groups. Let's say I named a HongKong dispatcher and bind it to agentA. Then a customer from hongkong required serverice and sent message to our server. The dispatcher will dispatcher the message to agentA and make a conservation.


+ Receive a email
    + set up postfix and it's callback.
    + deal with the received stream and decoded mail content and attachment and save to db.

+ We used Sidekiq to do the workers, RestClient to send a request, and gem `whever` to do shedules.


+ cetera  等等
+ try out 试用
+ design and model requirements
+ diff between
+ product manager 产品经理
+ prototype
+ evaluation service quality
+ company's base is far from my apartment. it cost 3 hours each day for traffic.




## introduce

My name is Mike Deng, I am 28 years old. I leaved office last month. I worked as developer for six years. Including 5 years backend and 1 year Full-stack. I have a lot of expriences in designning and modeling web application. The first language I used is C#. I delelop with it for 3 years. then I found it's has a lot of flaws. which including low productivity. And the minority of the opensource community. I kept finding and I turned to Ruby.It's has a lot of advantages.
and it has high productivities, and massive open source `gems`(or packages). As I joins ruby  developer community. For 3 years, I used Ruby on Rails to have finished a few of projects. I also used javascript, so I used Ruby on Rails as RESTful api provider and React as Front-end framework. It makes both backend and front-end codes clean and decent.



## saas

+ SaaS don't need for organizations to install and run applications on their own computers
+  This eliminates the expense of hardware,  maintenance. 
+  pay for this service on monthly or yearly versas
+ we provide updating the patch, or new features
+ ​



## analysis requirement

+ checking with PM if the requirement is regular, including 
  + avoid  it is `too huge to` control the time to deploy.  feature must be finish in one week.
  + avoid it's `duplicated`, two windows in the same form is acceptable
  + avoid it's `excessively designed`, should not be the complicated
  + find out the affected parts, modify one part, other parts are affected, modify them all.
+ work with front end
  + the api is documented by markdown
  + with params and url and description for them.
+ work with testing with jira
  + find the bug
  + fix it
  + or checking if it's requirement designer item or developer issue.
  + regression testing
+ After passing testing, it should deployed online

## reason to leave office

My former  work location is far away from my apartment。It cost me 3 hours in the traffic.

## Intro projects

+ the critical parts is a workflow of contracts used gem `workflow` 
+ it also use `organization info` as the base data
+ saleman fill the contract info and submit to the to financal staff
+ it will generate email as well as message and send the applied infomation to the financal staff
+ Finance staff review the contract info and submit to coo  ie `Chief Operating Officer`
+ COO will accept or rejected the contract.

### including

+ info messaging
+ privelige management
+ products management (im, callcenter, ticket), they may be sell as a whole or each part
+ email message
+ scheding job ( To checking the contract that is out of service ), whenever to generate message every 1 or 2 in the morning
+ capistrano and unicorn to deploy
+ include the front-end react component (mainly to make components to the html)



## what is virtual dom

React creates a tree of custom objects representing a part of the DOM. For example, instead of creating an actual DIV element containing a UL element, it creates a React.div object that contains a React.ul object. It can manipulate these objects very quickly without actually touching the real DOM or going through the DOM API. Then, when it renders a component, it uses this virtual DOM to figure out what it needs to do with the real DOM to get the two trees to match.

You can think of the virtual DOM like a blueprint. It contains all the details needed to construct the DOM, but because it `doesn't require all the heavyweight parts that go into a real DOM`, it can be created and changed much more easily.





Respc



two major process

Mount & Update

+ get init state
+ componentWillMount
+ componentDidMount
+ componentWillUpdate
+ componentDidUpdate
+ componentWillUnMount



最小知识

redux