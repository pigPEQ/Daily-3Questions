## `title`与`h1`、`b`与`strong`、`i`与`em`的区别
- `title`是网页的标题，一个页面只能存在一个;  
  `h1`是文章标题标签。
  
- `b`是文本加粗，是一个实体标签；  
  `strong`是字符加强语气，是一个逻辑标签。
  
- `i`是实体标签，使字符倾斜；   
   `em`是加强语气，默认样式是斜体；    
   为了符合CSS3的规范，尽量少使用`i`改用`em`。
   
 ## `style`写在`body`标签前与后的区别
 渲染页面时`DOM`与`CSS DOM`是并行的，两者结合生成render tree显示页面。  
 - `style`在`body`之前，渲染机制对样式**知根知底**，用了具体的标签直接用；
 - `style`在`body`之后，渲染机制对样式**一无所知**，到了具体的标签时就慌了，只能先显示无样式的部分，然后再去临时抱佛脚，最后补充样式。这种情况
 对DOM的渲染容易造成阻塞，产生FOUC(Flash of Unstyled Content)现象，即一瞬间的白屏或者样式的突然变化。在`HTML5.2`标准中，`style`放入`body`
 中是允许的。
 
 ## 排序算法题
 > **题目:** 通过一个输入框，输入一个自定义的数组，例如1,4,5,23,2,17,24,10000000。请把他按照中间高两边低进行排序，最后的结果是1,4,5,23,10000000,24,17,2，算法越准确越好，请注意左右翼数据数据的平衡性。
 ```javascript
    var sortArr=()=>{
      var input=prompt("请输入一组无重复的数字，数字间用逗号隔开")；
    }
    
 ```
