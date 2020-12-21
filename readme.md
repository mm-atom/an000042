# 配置anylogger-log4js

配置anylogger

配置文件 `log4js.json`

```json
{
	"appenders": {
		"console": {
			"type": "console"
		},
		"DAILYFILE": {
			"type": "dateFile",
			"filename": "./logs/mm.log",
			"pattern": ".yyyy-MM-dd-hh",
			"alwaysIncludePattern": false,
			"daysToKeep": 13,
			"maxLogSize": 20971520,
			"keepFileExt": true
		}
	},
	"categories": {
		"default": {
			"appenders": [
				"DAILYFILE",
				"console"
			],
			"level": "DEBUG"
		}
	}
}
```
