# DateTiemPicker

Based on Javascript date picker.

博客教程:

[手把手教你写Js日期时间选择器(1)-基本结构](http://blog.csdn.net/u012963788/article/details/52160333)

[手把手教你写Js日期时间选择器(2)-样式实现](http://blog.csdn.net/u012963788/article/details/52160618)

[手把手教你写Js日期时间选择器(3)-让控件滑动起来](http://blog.csdn.net/u012963788/article/details/52197584)

---
在线演示地址:

[在线演示](http://runjs.cn/detail/m0zy1iip)

[在线演示全屏](http://sandbox.runjs.cn/show/m0zy1iip)

[在线调试](http://runjs.cn/code/m0zy1iip)

##Image preview.


![demo.gif](screenshot/demo.gif)



##Usage

include datatime.css file.

	<script src="js/iscroll.js"></script>
	<script src="js/datetime.js"></script>

 	var datetime = new DateTime(document.getElementById("J_popup_offdelay"), null);

    datetime._init();
    datetime.bindEvent();



###With jQuery/Zepto


	<script src="js/jquery.js"></script>
	<script src="js/iscroll.js"></script>
	<script src="js/datetime.js"></script>
	<script src="js/JQuery.datetime.js"></script>
	$("#J_popup_offdelay").datetime();


### options

	{
        type: 'diy',//date,time,diy
        date: new Date(),
        minDate: new Date(),
        maxDate: new Date(),
        data: [{
            key: 'day',
            resource: ["上午", "下午"],
            value: "上午",
            unit: ''
        }, {
            key: 'hour',
            resource: ["21", "22", "23", "01", "02", "03", "04", "05", "06", "07"],
            value: "22",
            unit: ''
        }, {
            key: 'minute',
            resource: ["00", "30"],
            value: "00",
            unit: ''
        }],
        onChange: function (data) {
            console.log("call back", data);
        }
    }
