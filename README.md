# gulp

gulp本身是狼吞虎咽的的意思 最主要的是通过Transfrom Stream来实现文件的处理
然后在进行输出 Transform Stream是nodejs Stream的一种 是可读写的它会对传给它的对象进行一些操作。本质就是对文件(ts,sass,less...)写入到内存
进行任务的处理 在写出到文件中
gulp.src:获取文件
gulp.dest:写入文件
gulp.tasks:注册任务
gulp.watch:监听文件改动
gulp是一个自动构建工具 基于nodejs的自动任务运行器
通过注册的任务 自动的完成js/sass/less/html/css等文件的测试检查合并压缩格式化浏览器自动刷新部署文件生成并监听文件的改动后重复指定的这些操作

全局安装了gulp
npm install  --global gulp
作为项目的依赖将gulp引入项目
npm install gulp --save-dev
in project create gulpfile.js file
content
var gulp = require("gulp");
gulp.task("default",function(){
    console.info("Hello Gulp"); 
});
执行gulp
默认的名为default的任务(task)将会被运行 这个任务会输出Hello gulp in console
想要单独的执行某个任务:
gulp <task> <othertask>