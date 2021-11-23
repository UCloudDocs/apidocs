# 一键登录 - GetMobile

## 简介

一键登录









## 定义

### 公共参数

| 参数名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **Action**     | string  | 对应的 API 指令名称，当前 API 为 `GetMobile`                        | **Yes** |
| **PublicKey**  | string  | 用户公钥，可从 [控制台](https://console.ucloud.cn/uapi/apikey) 获取                                             | **Yes** |
| **Signature**  | string  | 根据公钥及 API 指令生成的用户签名，参见 [签名算法](api/summary/signature.md)  | **Yes** |

### 请求参数

| 参数名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **Region** | string | 地域。 参见 [地域和可用区列表](https://docs.ucloud.cn/api/summary/regionlist) |No|
| **Zone** | string | 可用区。参见 [可用区列表](https://docs.ucloud.cn/api/summary/regionlist) |No|
| **ProjectId** | string | 项目ID。不填写为默认项目，子帐号必须填写。 请参考[GetProjectList接口](https://docs.ucloud.cn/api/summary/get_project_list) |No|
| **BusinessId** | string | 业务ID |**Yes**|
| **Token** | string | token |**Yes**|

### 响应字段

| 字段名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **RetCode** | int | 返回状态码，为 0 则为成功返回，非 0 为失败 |**Yes**|
| **Action** | string | 操作指令名称 |**Yes**|
| **Message** | string | 返回错误消息，当 `RetCode` 非 0 时提供详细的描述信息 |No|
| **Data** | [*PhoneInfo*](#PhoneInfo) | 号码数据 |**Yes**|
| **ReqUuid** | string | 本次请求Uuid |No|

#### 数据模型


#### PhoneInfo

| 字段名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **Phone** | string | 返回的电话号码 |No|

## 示例

### 请求示例
    
```
https://api.ucloud.cn/?Action=GetMobile
&Region=cn-zj
&Zone=cn-zj-01
&ProjectId=qfPNcnKI
&BusinessId=INAOxWRF
&Token=ykRETQrW
```

### 响应示例
    
```json
{
  "Action": "GetMobileResponse",
  "Data": "mOVPoIKH",
  "Message": "AiOZMoxI",
  "ReqUuid": "JQzhScWC",
  "RetCode": 0
}
```




