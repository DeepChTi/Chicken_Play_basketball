# 鸡打篮球

---

我用了html，css，js来完成

```它会在屏幕中央显示一个篮球的emoji（🏀）和一个鸡的emoji（🐔）。当你点击篮球时，篮球会随机旋转一定角度。而当你点击鸡时，鸡会有一个垂直方向上的反弹效果。```

---

# 代码
[点我开始(https://deepchti.github.io/Chicken_Play_basketball/)]
## HTML

```html
<div class="basketball">🏀</div>
<div class="chicken">🐔</div>
```

## CSS

```css
body {
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            font-size: 5em;
        }
        
        .basketball {
            animation: bounce 1s infinite;
        }
        
        @keyframes bounce {
            0% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-40px);
            }
            100% {
                transform: translateY(0);
            }
        }
```

## JS

```js
// 等待页面加载完成后再执行代码
        document.addEventListener("DOMContentLoaded", function(event) {
            var basketball = document.querySelector('.basketball');
            var chicken = document.querySelector('.chicken');
            
            basketball.addEventListener('click', function() {
                // 添加一个随机的旋转角度
                var rotation = Math.floor(Math.random() * 360);
                basketball.style.transform = 'rotate(' + rotation + 'deg)';
            });

            chicken.addEventListener('click', function() {
                chicken.style.animation = 'bounce 1s infinite';
            });
        });
```

