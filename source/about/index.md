---
title: about
date: 2018-12-12 22:14:36
keywords: 关于
description: 
comments: false
photos: https://cdn.jsdelivr.net/gh/honjun/cdn@1.4/img/banner/about.jpg
---
{% raw %}
<div class="moe-mashiro" style="text-align:center; font-size: 50px; margin-bottom: 20px;">[かわいいのFloatcat]</div>
<div id="hello-mashiro" class="popcontainer" style="min-height: 300px; padding: 2px 6px 4px; background-color: rgba(242, 242, 242, 0.5); border-radius: 10px;">
  <center>
  <p>
  </p>
  <h4>
  与&nbsp;<ruby>
  Floatcat&nbsp;<rp>
  （</rp>
  <rt>
  Welcome</rt>
  <rp>
  ）</rp>
  </ruby>
  对话中...</h4>
  <p>
  </p>
  </center>
  <bot-ui></botui>
</div>
<script src="https://cdn.jsdelivr.net/vue/latest/vue.min.js"></script>
<script src="https://unpkg.com/botui/build/botui.min.js"></script>
<script>
function bot_ui_ini() {
    var botui = new BotUI("hello-mashiro");
    botui.message.add({
        delay: 800,
        content: "Hi, 亲爱的朋友👋"
    }).then(function () {
        botui.message.add({
            delay: 1100,
            content: "这里是Floatcat"
        }).then(function () {
            botui.message.add({
                delay: 1100,
                content: "一个可爱的女孩子~"
            }).then(function () {
                botui.action.button({
                    delay: 1600,
                    action: [{
                        text: "然后呢？ 😃",
                        value: "sure"
                    }, {
                        text: "少废话！ 🙄",
                        value: "skip"
                    }]
                }).then(function (a) {
                    "sure" == a.value && sure();
                    "skip" == a.value && end()
                })
            })
        })
    });
    var sure = function () {
            botui.message.add({
                delay: 600,
                content: "😘"
            }).then(function () {
                secondpart()
            })
        },
        end = function () {
            botui.message.add({
                delay: 600,
                content: "![...](https://view.moezx.cc/images/2018/05/06/a1c4cd0452528b572af37952489372b6.md.jpg)"
            })
        },
        secondpart = function () {
            botui.message.add({
                delay: 1500,
                content: "目前就读于广东工业大学"
            }).then(function () {
                botui.message.add({
                    delay: 1500,
                    content: "喜欢计算机与游戏…"
                }).then(function () {
                    botui.message.add({
                        delay: 1200,
                        content: "计算机需要Coder嘛"
                    }).then(function () {
                        botui.message.add({
                            delay: 1500,
                            content: "主攻 C 语言和 Java，略懂 python，偶尔也折腾 HTML/CSS/JavaScript"
                        }).then(function () {
                            botui.message.add({
                                delay: 1500,
                                content: "研究的方向是计算机科学与技术"
                            }).then(function () {
                                botui.message.add({
                                    delay: 1800,
                                    content: "喜欢游戏，希望有一天能成为顶尖游戏玩家"
                                }).then(function () {
                                    botui.action.button({
                                        delay: 1100,
                                        action: [{
                                            text: "为什么叫Floatcat呢？ 🤔",
                                            value: "why-mashiro"
                                        }]
                                    }).then(function (a) {
                                        thirdpart()
                                    })
                                })
                            })
                        })
                    })
                })
            })
        },
        thirdpart = function () {
            botui.message.add({
                delay: 1E3,
                content: "Floatcat是浮点猫的意思，浮点是编程语言里的一种数据类型，因为喜欢编程，就想到了这个名字~"
            }).then(function () {
                botui.action.button({
                    delay: 1500,
                    action: [{
                        text: "为什么是猫呢？ 🤔",
                        value: "why-cat"
                    }]
                }).then(function (a) {
                    fourthpart()
                })
            })
        },
        fourthpart = function () {
            botui.message.add({
                delay: 1E3,
                content: "因为喜欢猫啊… "
            }).then(function () {
                botui.message.add({
                    delay: 1100,
                    content: "我是一个猫控哦！"
                }).then(function () {
                    botui.action.button({
                        delay: 1500,
                        action: [{
                            text: "有什么想对用户说的吗",
                            value: "why-domain"
                        }]
                    }).then(function (a) {
                        fifthpart()
                    })
                })
            })
        },
        fifthpart = function () {
            botui.message.add({
                delay: 1E3,
                content: "坚持自己的梦想～"
            }).then(function () {
                botui.message.add({
                    delay: 1600,
                    content: "那么，仔细看看我的博客吧？ ^_^"
                })
            })
        } 
}
bot_ui_ini()
</script>
{% endraw %}