# describeResources


## 描述
获得资源与对应标签列表详情，不含资源名称和可用区。<br/>
注意查询cdn的资源时url中regionId必须指定为cn-all。<br/>
该接口目前不支持分页功能。


## 请求方式
POST

## 请求地址
https://resource-tag.jdcloud-api.com/v1/regions/{regionId}/tags:describeResources

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True| |Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**resourceVo**|ResourceReqVo|True| |资源标签参数对象|

### ResourceReqVo
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**serviceCodes**|String[]|False| |产品线名称列表<br>标签系统支持的产品线名称如下<br>- vm               disk        sqlserver  es          mongodb               ip<br>- memcached        redis       drds       rds         database              db_ro<br>- percona          percona_ro  mariadb    mariadb_ro  pg                    cdn<br>- nativecontainer  pod         zfs        jqs         kubernetesNodegroup   jcq<br>|
|**resourceIds**|String[]|False| |资源id列表|
|**tagFilters**|TagFilter[]|False| |标签过滤列表|
|**orderCondition**|String|False| |排序依据|
|**descOrAsc**|String|False|DESC|排序方向, 取值为ASC, DESC|
|**pageSize**|Integer|False| |每页记录数|
|**currentPage**|Integer|False| |当前页码|
### TagFilter
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**key**|String|False| |标签键|
|**values**|String[]|False| |标签值列表|
|**operator**|String|False|eq|操作选项, 默认为eq, 表示精确匹配|

## 返回参数
|名称|类型|描述|
|---|---|---|
|**result**|Result|响应结果对象|
|**requestId**|String|请求ID|

### Result
|名称|类型|描述|
|---|---|---|
|**data**|ResourceResVo|资源与对应标签列表详情|
### ResourceResVo
|名称|类型|描述|
|---|---|---|
|**pin**|String|用户pin|
|**region**|String|地域名称|
|**resourceTagMappingList**|ResourceTagMapping[]|资源标签详情列表|
### ResourceTagMapping
|名称|类型|描述|
|---|---|---|
|**jrn**|String|jrn本期不用, 默认为null|
|**serviceCode**|String|产品线名称|
|**resourceId**|String|资源id|
|**tags**|Tag[]|该资源绑定的标签组成的数组|
### Tag
|名称|类型|描述|
|---|---|---|
|**key**|String|标签键|
|**value**|String|标签值|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not found|
|**500**|Internal server error|
|**503**|Service unavailable|