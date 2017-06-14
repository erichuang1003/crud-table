
# rest-table

基于bootstrap table封装的一款表格组件

可快速配置生成一个具备CRUD功能的表格

通过restful接口规范调用后台接口


实例demo.js:



	$(function() {
		$('#container').restTable({
			creatable : true,
			updatable : true,
			deletable : 'multi',
			url : 'users/',
			columns : [
					{
						checkbox : true
					}, {
						title : 'ID',
						field : 'id',
						align : 'center',
						valign : 'middle',
						creatable : false,
						updatable : false
					}, {
						title : '名称',
						field : 'name',
						align : 'center',
						valign : 'middle'
					}, {
						title : '年龄',
						field : 'age',
						align : 'center',
						valign : 'middle',
						type : 'number'
					}, {
						title : '类型',
						field : 'type',
						align : 'center',
						valign : 'middle',
						editor : {
							type : 'select',
							data : [
									1, 2, 3
							]
						}
					}, {
						title : '时间',
						field : 'date',
						align : 'center',
						valign : 'middle',
						editor : {
							type : 'datetime',
							format : 'yyyy-mm-dd'
						}
					}
			]
		});
	
	});


