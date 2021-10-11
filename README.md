# OA办公系统_人事管理系统

## 介绍
这是一套智能OA办公系统，里面包含了人事管理系统，这套功能的主干都已经完成，大多数功能用到的都是ajax技术，极个别界面采用传统MVC方法。代码规范化，基本上每个类和每个方法都写有注释。

目前这套系统有一套毕业设计论文，包括开题报告、文献综述、一稿、二稿及终稿，维普查重率6%左右，大学生毕业论文不会录入知网和维普等查重系统，可以用于毕业设计。

提供后续服务，包括代码讲解，疑难解答和答辩的注意事项，有需要可以联系`863772270`

## 1.前言

本套系统主要实现的是OA办公系统中一些常用发功能，还有一些功能因为时间的原因没有开发，但主线功能基本完善。前端页面模板用的是GitHub上面一位老兄OA系统办公模板，但功能上面的话我都进行了重新编写，用自己的代码方式改了过来，并添加了很多功能点。

## 2.准备工作

**开发环境**：MySQL8.0，JDK1.8，Tomcat9.0

**开发工具**：eclipse2020，Navicat15，HBuilder X，vscode。

**开发语言**：java、html、css、javascript

**第三方工具库**：hutool、fastjson、jstl、bootstrap、jQuery、echarts、font-awesome

## 3.项目结构



![在这里插入图片描述](https://img-blog.csdnimg.cn/20200906235113779.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQyMzc2NjE3,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200906235113770.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQyMzc2NjE3,size_16,color_FFFFFF,t_70#pic_center)


## 4.部分界面截图

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200906235138142.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQyMzc2NjE3,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200906235138182.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQyMzc2NjE3,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020090623513891.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQyMzc2NjE3,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020090623513873.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQyMzc2NjE3,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020090623513853.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQyMzc2NjE3,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020090623513849.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQyMzc2NjE3,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020090623513837.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQyMzc2NjE3,size_16,color_FFFFFF,t_70#pic_center)
![在这里插入图片描述](https://img-blog.csdnimg.cn/202009062351383.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQyMzc2NjE3,size_16,color_FFFFFF,t_70#pic_center)


由于系统的页面很多，就不一一截图了，总体的功能较为丰富，主线功能都完成。在人事管理中心的一个管理界面，对员工的一些信息进行了数据可视化分析，用到了echarts.js库，主要是把员工的学历、居住地、毕业学校、专业的数据进行了分析。

## 5.部分代码分析

### 5.1.1 ajax登录和添加员工功能

这部分实现的原理在[《基于JavaEE(JSP)的共享资料平台的设计与实现》](https://blog.csdn.net/qq_42376617/article/details/108309396)的第五点有说明，在这边就不继续介绍了。其JS代码部分基本上都是一样，唯一有差别的就是在jsp文件中，表单的格式不一样罢了。

### 5.1.2 考勤打卡功能

这是打卡日历图的代码，实现的功能为打卡日历图的显示，上班打卡一次，刷新一次会报红，因为没有继续打卡第二次，只有下班打卡后才会显示正常，下面环形也会显示全勤。日历图展示的时间数据是取最早打卡记录和最晚打卡记录，

数据库查询语句为`SELECT EMP_ID,ATT_DATE,min(ATT_SIGNIN) as ATT_SIGNIN,max(ATT_SIGNOUT) as ATT_SIGNOUT from ATTENDANCE GROUP BY ATT_DATE `,就用到了最大的时间和最小的时间。

```js
    /**
	打卡日历模块
 */
(function(undefined) {
	var _global;
	//工具函数
	//配置合并
	function extend(def, opt, override) {
		for(var k in opt) {
			if(opt.hasOwnProperty(k) && (!def.hasOwnProperty(k) || override)) {
				def[k] = opt[k]
			}
		}
		return def;
	}
	//日期格式化
	function formartDate(y, m, d, symbol) {
		symbol = symbol || '-';
		m = (m.toString())[1] ? m : '0' + m;
		d = (d.toString())[1] ? d : '0' + d;
		return y + symbol + m + symbol + d
	}

	function Schedule(opt) {
		var def = {},
			opt = extend(def, opt, true),
			curDate = opt.date ? new Date(opt.date) : new Date(),
			year = opt.selectYear || curDate.getFullYear(),
			month = opt.selectMonth || curDate.getMonth(),
			day = curDate.getDate(),
			currentYear = curDate.getFullYear(),
			currentMonth = curDate.getMonth(),
			currentDay = curDate.getDate(),
			selectedDate = '',
			//缺勤
			qqDate = opt.qqDate || "",
			zcDate = opt.zcDate || "",
			el = document.querySelector(opt.el) || document.querySelector('body'),
			_this = this;
		var bindEvent = function() {
//			if(el.dataset['cc']){
				el.addEventListener('click', function(e) {
					switch(e.target.id) {
						case 'nextMonth':
							_this.nextMonthFun();
							break;
						case 'nextYear':
							_this.nextYearFun();
							break;
						case 'prevMonth':
							_this.prevMonthFun();
							break;
						case 'prevYear':
							_this.prevYearFun();
							break;
						default:
							break;
					};
					if(e.target.className.indexOf('currentDate') > -1) {
						opt.clickCb && opt.clickCb(year, month + 1, e.target.innerHTML,e.target);
						selectedDate = e.target.title;
						day = e.target.innerHTML;
						render();
					}
				}, false)
//				el.dataset['cc']=1;
//			}
		}
		var init = function() {
			var scheduleHd = '<div class="schedule-hd">' +
				'<div>' +
				'<span class="arrow icon iconfont icon-112leftarrowhead" id="prevMonth"></span>' +
				'</div>' +
				'<div class="today">' + year + "年" + (month + 1) + "月" + '</div>' +
				'<div>' +
				'<span class="arrow icon iconfont icon-111arrowheadright" id="nextMonth"></span>' +
				'</div>' +
				'</div>'
			var scheduleWeek = '<ul class="week-ul ul-box clearfix">' +
				'<li>日</li>' +
				'<li>一</li>' +
				'<li>二</li>' +
				'<li>三</li>' +
				'<li>四</li>' +
				'<li>五</li>' +
				'<li>六</li>' +
				'</ul>'
			var scheduleBd = '<ul class="schedule-bd ul-box clearfix" ></ul>';
			el.innerHTML = scheduleHd + scheduleWeek + scheduleBd;
			bindEvent();
			render();
		}
		var render = function() {
			var fullDay = new Date(year, month + 1, 0).getDate(), //当月总天数
				startWeek = new Date(year, month, 1).getDay(), //当月第一天是周几
				total = (fullDay + startWeek) % 7 == 0 ? (fullDay + startWeek) : fullDay + startWeek + (7 - (fullDay + startWeek) % 7), //元素总个数
				lastMonthDay = new Date(year, month, 0).getDate(), //上月最后一天
				eleTemp = [];
			for(var i = 0; i < total; i++) {
				if(i < startWeek) {
					var nowDate = formartDate(year, month, ((lastMonthDay - startWeek) + 1 + i), '-');
					var addClass = '';
					
					eleTemp.push('<li class="other-month"><span class="dayStyle ' + addClass + '">' + (lastMonthDay - startWeek + 1 + i) + '</span></li>')
				} else if(i < (startWeek + fullDay)) {
					var nowDate = formartDate(year, month + 1, (i + 1 - startWeek), '-');
					var addClass = '';
					var attSignin = '';
					var attSignout = '';
					//					selectedDate == nowDate && (addClass = 'selected-style');
					for(var j = 0; j < zcDate.length; j++) {
						zcDate[j].attDate == nowDate && (addClass = 'zc_day', attSignin = zcDate[j].attSignin, attSignout = zcDate[j].attSignout);
					}
					for(var z = 0; z < qqDate.length; z++) {
						qqDate[z].attDate == nowDate && (addClass = 'qq-style', attSignin = qqDate[z].attSignin, attSignout = qqDate[z].attSignout);
					}
					//					formartDate(currentYear,currentMonth+1,currentDay,'-') == nowDate && (addClass = 'today-flag');
					eleTemp.push('<li class="current-month" ><span  class="currentDate dayStyle ' + addClass + '">' + (i + 1 - startWeek) + '</span><div class="day_time"><div>上班：' + attSignin + '</div><div>下班：' + attSignout + '</div></li>')
				} else {
					eleTemp.push('<li class="other-month"><span class="dayStyle">' + (i + 1 - (startWeek + fullDay)) + '</span></li>')
				}
			}
			el.querySelector('.schedule-bd').innerHTML = eleTemp.join('');
			el.querySelector('.today').innerHTML = year + "年" + (month + 1) + "月";
		};
		this.nextMonthFun = function() {
				if(month + 1 > 11) {
					year += 1;
					month = 0;
				} else {
					month += 1;
				}
				render();
				opt.nextMonthCb && opt.nextMonthCb(year, month + 1, day);
			},
			this.nextYearFun = function() {
				year += 1;
				render();
				opt.nextYeayCb && opt.nextYeayCb(year, month + 1, day);
			},
			this.prevMonthFun = function() {
				if(month - 1 < 0) {
					year -= 1;
					month = 11;
				} else {
					month -= 1;
				}
				render();
				opt.prevMonthCb && opt.prevMonthCb(year, month + 1, day);
			},
			this.prevYearFun = function() {
				year -= 1;
				render();
				opt.prevYearCb && opt.prevYearCb(year, month + 1, day);
			}
		init();
	}
	//将插件暴露给全局对象
	_global = (function() {
		return this || (0, eval)('this')
	}());
	if(typeof module !== 'undefined' && module.exports) {
		module.exports = Schedule;
	} else if(typeof define === "function" && define.amd) {
		define(function() {
			return Schedule;
		})
	} else {
		!('Schedule' in _global) && (_global.Schedule = Schedule);
	}

}());
```

### 5.1.3 ajax与Bootstrap Table实现表格内容的读写与分页

这里的列表代码以部门管理为例进行演示。



这是前端table的写法，主要是把表头给写出来，然后利用bootstrap的写法，在js里面写实现方法，还是比较方便的。下面就来一一讲解实现过程。

```html
<table id="datagrid" class="table table-bordered table-striped table-hover">
    <thead>
        <tr>
            <th data-width="60" data-align="center"
                data-formatter="indexFormatter">#</th>
            <th data-field="deptId" data-align="center">部门编号</th>
            <th data-field="deptName" data-align="center">部门名称</th>
            <th data-field="deptUserid" data-align="center">负责人</th>
            <th data-field="deptCreatetime" data-align="center" data-formatter="dateFormatter">创建时间</th>
            <th data-field="deptId" data-class="p-1" data-width="150"
                data-align="center" data-formatter="optionFormatter">操作</th>
        </tr>
    </thead>
</table>
```

<details><summary>CLICK ME</summary> <pre><code>
```java
</code></pre></details>


然后在其他`<th></th>`标签中，有一个`data-field`属性，这里表达的是这一列所需要的展示的值，也就是从数据库返回的值显示的内容。

在创建时间的`<th></th>`的标签里面，写了一个`data-formatter="dateFormatter"`,和上面的原理一样，在下面的js代码找到dateFormatter函数。主要是对数据库传来的时间进行格式化展示。

```js
/**
	装载下拉框的角色列表
 */
var searchDeptForm = $(document.forms.searchDeptForm);
var searchDeptForms = document.forms.searchDeptForm;

//表单提交事件
searchDeptForms.onsubmit = ()=>{
	$.post(
		searchDeptForms.action,
		sys.form.param(searchDeptForms).toString(),
		function(data){
			if(data.code==200){
				//sys.js库中定义的方法，可以弹出提示界面
				sys.toastr.success("查询成功");
			}else{
				sys.toastr.error(data.message);
			}
		},"json"
	);
	return false;
}

// 获取部门下拉框的数据
var deptIdSelect = $(document.forms.searchDeptForm.deptIdSelect);
$.get(
	"department.let?action=listDepts",
	function(data){
		for(let dept of data) {
			deptIdSelect.append(`<option value="${dept.deptId}">${dept.deptName}</option>`);
		}
	},"json"
);


//保存查询条件
var searchParams = new URLSearchParams();
searchDeptForm.on("submit",function(){
	searchParams = sys.form.param(searchDeptForm[0]);
	datagrid.bootstrapTable("refresh",{pageNumber:1});
	return false;
});

/**
	表格内容填充方式，从数据库请求的数据，填充到表格中
*/
var datagrid = $("#datagrid").bootstrapTable({
	url: "department.let?action=page",
	dataField: "list",//rows
	totalField: "total",
	queryParamsType: "",//limit
	pagination: true,
	sidePagination: "server",//client
	queryParams:function(params) { 
	  for(let name of searchParams.keys()){//添加搜索条件
		  params[name]=searchParams.get(name);
	  }
	  return params 
    }
});

/**
	列表最前面加索引
 */
var indexFormatter = function(value, row, index, fieldName) {
	return index + 1;
}

/**
	给时间设置0
 */
function addZero(n) {
	return n < 10 ? '0' + n : '' + n;
};

/**
	格式化时间
 */
var dateFormatter = function(value, row, index, fieldName) {
	var date = new Date(value);
	var time = date.getFullYear() + "-" + addZero(date.getMonth() + 1) + "-" + addZero(date.getDate());
	return time;
}

/**
 * 格式化表格操作菜单
 */
var optionFormatter = function(value, row, index) {
	return `<div class="dropdown">
  <button class="btn btn-outline-primary btn-block dropdown-toggle" type="button" data-toggle="dropdown">
    操作
  </button>
  <div class="dropdown-menu dropdown-menu-right">
    <a class="dropdown-item"   href="department.let?action=getDeptInfo&deptId=${value}">查看&修改</a>
    <a class="dropdown-item _delete" data-index="${index}" href="javascript:void(0);">删除</a>
  </div>
</div>`;
}

/**
	操作按钮
 */
datagrid.on("click", "._delete", function() {//删除
	let obj = $(this);
	let index = obj.data("index");//data-index
	let row = datagrid.bootstrapTable("getData")[index];
	sys.confirm(`您确定要删除[${row.deptName}]吗？`, function(r) {
		if (r) {
			$.post(
				"department.let?action=delete",
				{ "deptId": row.deptId },
				function(data) {
					if (data.code == 200) {
						sys.toastr.success(`删除用户[${row.deptName}]成功`);
						datagrid.bootstrapTable("refresh");
					} else {
						sys.toastr.error(data.message);
					}
				}, "json"
			);
		}
	});
});
```

### 5.1.4 员工各类信息统计Echarts代码

环状比例图的实现代码，主要用的是echarts库。传入的数据有三种`TextData,DigitalData,titleText`，分别为图例数据、员工详情数据、该图形的标题数据。

```js
function EmpCityChart(TextData,DigitalData,titleText) {
    var myChart = echarts.init(document.getElementById('empCity'));
    var img = 'data:image/png;base64,iVBORw0K....VORK5CYII=';
    var trafficWay = DigitalData;
    var data = [];
    var color=['#00ffff','#00cfff','#006ced','#ffe000','#ffa800','#ff5b00','#ff3000']
    for (var i = 0; i < trafficWay.length; i++) {
        data.push({
            value: trafficWay[i].value,
            name: trafficWay[i].name,
            itemStyle: {
                normal: {
                    borderWidth: 5,
                    shadowBlur: 20,
                    borderColor:color[i],
                    shadowColor: color[i]
                }
            }
        }, {
            value: 2,
            name: '',
            itemStyle: {
                normal: {
                    label: {
                        show: false
                    },
                    labelLine: {
                        show: false
                    },
                    color: 'rgba(0, 0, 0, 0)',
                    borderColor: 'rgba(0, 0, 0, 0)',
                    borderWidth: 0
                }
            }
        });
    }
    var seriesOption = [{
        name: '',
        type: 'pie',
        clockWise: false,
        radius: [105, 109],
        hoverAnimation: false,
        itemStyle: {
            normal: {
                label: {
                    show: true,
                    position: 'outside',
                    color: '#ddd',
                    formatter: function(params) {
                        var percent = 0;
                        var total = 0;
                        for (var i = 0; i < trafficWay.length; i++) {
                            total += trafficWay[i].value;
                        }
                        percent = ((params.value / total) * 100).toFixed(0);
                        if(params.name !== '') {
                            return titleText+'：' + params.name + '\n' + '\n' + '占百分比：' + percent + '%';
                        }else {
                            return '';
                        }
                    },
                },
                labelLine: {
                    length:30,
                    length2:100,
                    show: true,
                    color:'#00ffff'
                }
            }
        },
        data: data
    }];
    option = {
        backgroundColor: '#5e7c85',
        color : color,
        title: {
            text:titleText,
            top: '48%',
            textAlign: "center",
            left: "49%",
            textStyle: {
                color: '#fff',
                fontSize: 22,
                fontWeight: '400'
            }
        },
        graphic: {
            elements: [{
                type: "image",
                z: 3,
                style: {
                    image: img,
                    width: 178,
                    height: 178
                },
                left: 'center',
                top:  'center',
                position: [100, 100]
            }]
        },
        tooltip: {
            show: false
        },
        legend: {
            icon: "circle",
            orient: 'horizontal',
            x: 'center',
            data:TextData,
            top: 10,
            align: 'left',
            textStyle: {
                color: "#fff"
            },
            itemGap: 20
        },
        toolbox: {
            show: false
        },
        series: seriesOption
    }
    myChart.setOption(option);
}
```

ajax请求数据，这里请求的数据是员工的岗位数据分析数据，将获得的数据进行格式的一些转换，然后调用上面的函数，就可以正常显示图形了。

```js
function empDegree(){
	$.get(
		"chartData.let?action=getEmpDegreeData",
		function(data){
			var empText=[];
			var empData=[];
			for(let i=0;i<data.data.length;i++){
				empText.push(data.data[i].empTiptopdegree);
				empData.push({name:data.data[i].empTiptopdegree,value:data.data[i].empData*100});
			}
			EmpCityChart(empText,empData,"最高学历")
		},"json"
	);
}
```

servlet实现获取数据。这里写了SQL语句是因为在service和dao包中的实现类用的是同一个方法，只需要传入不同的SQL语句和异常代号和异常信息就可以了。

```java
private ChartDataService chartDataService = new ChartDataServiceImpl();

/**
* -获取员工的学历数据
* @return
*/
public R<?> getEmpDegreeData(){
    String sql = "select EMP_TIPTOPDEGREE,COUNT(EMP_TIPTOPDEGREE) as EMP_DATA from EMPLOYEE GROUP BY EMP_TIPTOPDEGREE";
    List<Employee> empData = chartDataService.getEmpData(sql,1001,"获取员工学历数据失败");
    return R.ok(empData);
}
```

ChartDataDAO.java实现

```java
/**
* -由于代码非常相似，所以只需要根据SQL语句不同查询不同的字段就行，这里查询的是员工的数据
* @return
* @throws SQLException 
*/
public List<Employee> getEmpData(String sql) throws SQLException {
    List<Object> params = new ArrayList<Object>();
    return DBUtil.list(sql, Employee.class, params.toArray());
}
```

## 6.总结

以上的系统主线功能基本完成，从GitHub大佬用的模板改进了全部功能，现在找不到这个GitHub的地址是什么了，如果有侵权请联系。用来学习的话，能够把全部代码总一遍，基本上可以学会所有的javaee知识，如果JavaScript底子好的话，还能够深入的研究一下ajax代码。ajax代码比传统MVC好用多了。

好了，这次的项目分享到此也差不多了。觉得小弟写的不错的话，可以点赞加关注一下，谢谢！有需要源码的小伙伴也可以搜索**企鹅号863772270**，编码不易，请作者喝瓶水即可。
