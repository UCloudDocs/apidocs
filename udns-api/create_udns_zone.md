# 创建域名 - CreateUDNSZone

## 简介

创建域名






## 使用方法

您可以选择以下方式中的任意一种，发起 API 请求：
- [UAPI 浏览器](https://console.ucloud.cn/uapi/detail?id=CreateUDNSZone)
- [CloudShell 云命令行](https://shell.ucloud.cn/)


## 定义

### 公共参数

| 参数名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **Action**     | string  | 对应的 API 指令名称，当前 API 为 `CreateUDNSZone`                        | **Yes** |
| **PublicKey**  | string  | 用户公钥，可从 [控制台](https://console.ucloud.cn/uapi/apikey) 获取                                             | **Yes** |
| **Signature**  | string  | 根据公钥及 API 指令生成的用户签名，参见 [签名算法](api/summary/signature.md)  | **Yes** |

### 请求参数

| 参数名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **Region** | string | 地域。 参见 [地域和可用区列表](https://docs.ucloud.cn/api/summary/regionlist) |**Yes**|
| **ProjectId** | string | 项目ID。不填写为默认项目，子帐号必须填写。 请参考[GetProjectList接口](https://docs.ucloud.cn/api/summary/get_project_list) |No|
| **DNSZoneName** | string | 域名字符串 |**Yes**|
| **Type** | string | 域名类型。枚举值，“private”，内网DNS；“public”，公网DNS，暂只支持private。 |**Yes**|
| **Tag** | string | 所属业务组名称 |No|
| **Remark** | string | 备注 |No|
| **IsRecursionEnabled** | string | 是否支持迭代。枚举值,"enable",支持迭代; "disable",不支持迭代 |No|
| **Quantity** | int | 购买时长，默认为1 |No|
| **ChargeType** | string | 付费方式, 枚举值为: Year, 按年付费; Month, 按月付费; Dynamic, 按需付费，默认为按月付费 |No|
| **CouponId** | string | 代金券ID，默认不使用 |No|

### 响应字段

| 字段名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **RetCode** | int | 返回状态码，为 0 则为成功返回，非 0 为失败 |**Yes**|
| **Action** | string | 操作指令名称 |**Yes**|
| **Message** | string | 返回错误消息，当 `RetCode` 非 0 时提供详细的描述信息 |No|
| **DNSZoneId** | string | 域名资源ID |**Yes**|




## 示例

### 请求示例
    
```
https://api.ucloud.cn/?Action=CreateUDNSZone
&Region=cn-zj
&ProjectId=OGMaUpAY
&DNSZoneName=ouSidlfS
&Type=rmJzsOXr
&IsRecursionEnabled=fEuQBzyM
&Tag=tYekqMYL
&Remark=EWtpMzaK
&Quantity=2
&ChargeType=EKGnjVoE
&CouponId=aTtyjaOH
```

### 响应示例
    
```json
{
  "Action": "CreateUDNSZoneResponse",
  "DNSZoneId": "PDQFXUrQ",
  "RetCode": 0
}
```




