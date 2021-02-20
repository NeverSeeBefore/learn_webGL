# learn_webGL

webGl（图形库），是一种jsAPI
openGl
GLSL    着色器语言

webGl 是图形学规范要学习的是webglAPI
webGl 是 js 与 GLSL 两种程序组成的
webGl 是 将3d数据显示到2d平面上
webGl 使用gpu和cpu


webGL 优点:
1. 只要一个编辑器和浏览器就可以编辑一个三位图形程序
2. 通过使用web技术发布三位图形程序显示
3. 充分利用浏览器功能

### clearColor 与 clear

必须强调 glClearColor只起到Set的作用，并不Clear任何！不要混淆~2. glClearColor 的作用是，指定刷新颜色缓冲区时所用的颜色。所以，完成一个刷新过程是要 glClearColor(COLOR) 与 glClear(GL_COLOR_BUFFER_BIT) 配合使用。glClearColor(0.0, 0.0, 1.0, 1.0);//蓝色
glClear(GL_COLOR_BUFFER_BIT);
清除颜色缓冲区的作用是，防止缓冲区中原有的颜色信息影响本次绘图（注意！即使认为可以直接覆盖原值，也是有可能会影响的），当绘图区域为整个窗口时，就是通常看到的，颜色缓冲区的清除值就是窗口的背景颜色。所以，这两条清除指令并不是必须的：比如对于静态画面只需要设置一次，比如不需要背景色/背景色为白色。4. glClear 比手动涂抹一个背景画布效率高且省力，所以通常使用这种方式。