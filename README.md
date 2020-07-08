# MCSM

用于企业内部系统常用功能

管理系统集成? 分发库?

## 参考标准

[12factor](https://12factor.net/zh_cn/)

## Git Branch

- master			# README
- mcsm				# 主分支
- mcsm-template		# 工具包模版
- mcsm-msutil		# Office工具包
- mcsm-scheduler	# Scheduler 工具包
- mcsm-database		# Database 工具包
- mcsm-mq			# Message 工具包
- mcsm-mail			# Mail 工具包
- mcsm-flow			# 流程引擎工具包
- mcsm-*			# XX 工具包

### mcsm-config ( 配置包 )

配置方式

- 本地			# 简单应用
- 远程
- 第三方库
  - [dynaconf](https://github.com/rochacbruno/dynaconf)

文件类型

- ini		# 主要因为基础库
- yml		# 可读性
- json		# 暂时不考虑

设想

```
app
	config
		default.yml
		testing.yml
		development.yml
		production.yml

		redis.yml
		database.yml
	setting.cfg
		CONFIG=default.yml
	main.py
		from mscm_config import config
		config.read()
```

