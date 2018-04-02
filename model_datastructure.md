
	CREATE TABLE `tb_sku_code` (
	  `id` int(10) NOT NULL AUTO_INCREMENT COMMENT 'SKUID',
	  `code` varchar(2) NOT NULL COMMENT 'SKU的代码',
	  `pid` int(10) NOT NULL COMMENT '上级SKU代码',
	  `name` varchar(25) DEFAULT NULL COMMENT '代码名称',
	  `level` int(1) DEFAULT NULL COMMENT 'sku级别：1-LI;2-L2;3;L3;4-L4',
	  `type` int(1) DEFAULT NULL COMMENT 'sku代码类别：1-销售模块;2-OEM销售模块;3-销售配件;4-配件销售;5-物料;6-外部服务;7-内部服务',
	  `status` int(1) DEFAULT NULL COMMENT 'SKU代码状态：0-生效，1-生效',
	  `createtime` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP,
	  PRIMARY KEY (`id`)
	) ENGINE=InnoDB AUTO_INCREMENT=769 DEFAULT CHARSET=utf8;


	CREATE TABLE `tb_sku` (
	  `id` int(10) NOT NULL AUTO_INCREMENT,
	  `kom_id` int(10) DEFAULT NULL COMMENT 'kom系统的ID',
	  `l1` int(10) NOT NULL COMMENT '一级编码ID',
	  `l2` int(10) NOT NULL COMMENT '二级编码ID',
	  `l3` int(10) NOT NULL COMMENT '三级编码ID',
	  `l4` int(10) NOT NULL COMMENT '四级编码ID',
	  `l5` varchar(10) DEFAULT NULL COMMENT '五级编码ID',
	  `sku` varchar(25) DEFAULT NULL COMMENT 'sku code',
	  `type` int(2) DEFAULT NULL COMMENT 'sku代码类别：0 服务；1 销售；3 物料；',
	  `name` varchar(255) DEFAULT NULL COMMENT 'sku名',
	  `createtime` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP,
	  `endtime` datetime DEFAULT NULL ON UPDATE CURRENT_TIMESTAMP,
	  `status` int(1) DEFAULT NULL COMMENT 'SKU代码状态：0-生效，1-生效',
	  PRIMARY KEY (`id`)
	) ENGINE=InnoDB AUTO_INCREMENT=2 DEFAULT CHARSET=utf8;