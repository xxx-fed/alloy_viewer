# alloy_viewer H5图片查看器



## 例子

[https://alloyteam.github.io/AlloyViewer/examples/](https://alloyteam.github.io/AlloyViewer/examples/)


## 使用说明



	// 例 1:
	
	import React, { Component } from 'react'
	import ImageView from 'react-imageview'
	
	import 'react-imageview/dist/react-imageview.min.css'
	
	class Main extends Component {
	    state = {
	        showViewer: false
	    }
	    render() {
	        const imagelist = ['./1.png','./2.png','./3.png','./4.png']
	        return (
	            <div>
	                {
	                    !!this.state.showViewer && <ImageView imagelist={imagelist} close={this.close.bind(this)} />
	                }
	                <button onClick={e=>this.show()}>click me to show Alert</button>
	            </div>
	        )
	    }
	    show() {
	        this.setState({ showViewer: true })
	    }
	    close() {
	        this.setState({ showViewer: false})
	    }
	}
	
	// 例 2（推荐使用）:
	
	import { SingleImgView } from 'react-imageview'
	import 'react-imageview/dist/react-imageview.min.css'
	
	const imagelist = ['./1.png','./2.png','./3.png','./4.png']
	
	// 仅创建一个ImageView实例
	SingleImgView.show({ 
	    imagelist, 
	    close: () => { SingleImgView.hide() } 
	});

## 配置说明

<table>
<thead>
<tr>
<th align="left">参数</th>
<th align="left">类型</th>
<th align="left">描述</th>
<th align="left">必需</th>
<th align="left">默认值</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">imagelist</td>
<td align="left">array</td>
<td align="left">要预览的图片列表</td>
<td align="left">是</td>
<td align="left">无</td>
</tr>
<tr>
<td align="left">current</td>
<td align="left">number</td>
<td align="left">当前展示的图片序号（从0开始）</td>
<td align="left">否</td>
<td align="left">0</td>
</tr>
<tr>
<td align="left">close</td>
<td align="left">function</td>
<td align="left">图片查看器关闭方法</td>
<td align="left">是</td>
<td align="left"></td>
</tr>
<tr>
<td align="left">gap</td>
<td align="left">number</td>
<td align="left">轮播图间距</td>
<td align="left">否</td>
<td align="left">30</td>
</tr>
<tr>
<td align="left">maxScale</td>
<td align="left">number</td>
<td align="left">最大缩放倍数</td>
<td align="left">否</td>
<td align="left">2</td>
</tr>
<tr>
<td align="left">disablePinch</td>
<td align="left">bool</td>
<td align="left">禁用缩小放大</td>
<td align="left">否</td>
<td align="left">false</td>
</tr>
<tr>
<td align="left">enableRotate</td>
<td align="left">bool</td>
<td align="left">启用旋转</td>
<td align="left">否(默认关闭)</td>
<td align="left">false</td>
</tr>
<tr>
<td align="left">disableDoubleTap</td>
<td align="left">bool</td>
<td align="left">禁用双击放大</td>
<td align="left">否</td>
<td align="left">false</td>
</tr>
<tr>
<td align="left">initCallback</td>
<td align="left">function</td>
<td align="left">初始化后回调</td>
<td align="left">否</td>
<td align="left"></td>
</tr>
<tr>
<td align="left">longTap</td>
<td align="left">function</td>
<td align="left">长按回调</td>
<td align="left">否</td>
<td align="left"></td>
</tr>
<tr>
<td align="left">changeIndex</td>
<td align="left">function</td>
<td align="left">轮播后回调</td>
<td align="left">否</td>
<td align="left"></td>
</tr>
</tbody>
</table>

## 官方的

[https://github.com/AlloyTeam/AlloyViewer](https://github.com/AlloyTeam/AlloyViewer)


