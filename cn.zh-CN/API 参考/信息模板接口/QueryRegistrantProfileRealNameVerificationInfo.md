# QueryRegistrantProfileRealNameVerificationInfo {#concept_yfg_2kc_b2b .concept}

QueryRegistrantProfileRealNameVerificationInfo查询域名信息模板实名认证资料。

## 请求参数 {#section_uy4_qkc_b2b .section}

|参数|类型|是否必选|示例值|描述|
|RegistrantProfileId|Long|是|123456|域名信息模板编号。|
|FetchImage|Boolean|否|false|是否获取实名认证图片。|
|Lang|String|否|en|接口返回错误信息语言。枚举值范围：zh 中文；en 英文。默认为 en。|
|UserClientIp|String|否|127.0.0.1|用户IP。|

## 返回参数 {#section_q1l_tkc_b2b .section}

|参数|类型|示例值|描述|
|RequestId|String|4D73432C-7600-4779-ACBB-C3B5CA145D32|唯一请求识别码。|
|SubmissionDate|String|2017-05-22 19:04:49|提交时间。|
|ModificationDate|String|2017-05-22 19:04:49|更新时间。|
|IdentityCredential|String|dGVzdA==|采用base64编码的实名认证资料。|
|RegistrantProfileId|Long|123456|信息模板编号。|
|IdentityCredentialNo|String|123456|实名认证资料证件号码。|
|IdentityCredentialType|String|SFZ|实名认证证件类型，取值： -   SFZ：身份证
-   HZ：护照
-   YYZZ：营业执照
-   ORG：组织机构代码证
-   XYDM：统一社会信用代码证书
-   TXZ：港澳居民来往内地通行证

 如果您使用的证件不在上述范围中，请参考 [支持实名认证的证件类型](cn.zh-CN/API 参考/附录/支持实名认证的证件类型.md#)查看相应的证件类型取值。 **说明：** 请务必选择与您传入的证件相符的证件类型。

 |

## 示例 {#section_u2g_j5s_b2b .section}

**请求示例**

``` {#codeblock_jvv_aft_rio}
/?Action=QueryRegistrantProfileRealNameVerificationInfo
&RegistrantProfileId=123456
&FetchImage=false
&<公共请求参数>
```

**正常返回示例**

-   XML示例

    ``` {#codeblock_oyh_6si_pzm}
    <QueryRegistrantProfileRealNameVerificationInfoResponse>
      <RegistrantProfileId>123456</RegistrantProfileId>
      <RequestId>175FE8E4-309A-466B-AA84-DE7E2A19C948</RequestId>
      <ModificationDate>2017-05-22 19:04:49</ModificationDate>
      <IdentityCredentialType>SFZ</IdentityCredentialType>
      <IdentityCredentialNo>1234567890123456</IdentityCredentialNo>
      <SubmissionDate>2017-05-22 19:04:49</SubmissionDate>
    </QueryRegistrantProfileRealNameVerificationInfoResponse>
    ```

-   JSON示例

    ``` {#codeblock_gvx_nry_hcd}
    {
        "IdentityCredentialNo":"411111111111111",
        "IdentityCredentialType":"SFZ",
        "ModificationDate":"2017-05-22 19:04:49",
        "RegistrantProfileId":123456,
        "RequestId":"4D73432C-7600-4779-ACBB-C3B5CA145D32",
        "SubmissionDate":"2017-05-22 19:04:49"
    }
    ```


**错误返回示例**

-   XML示例

    ``` {#codeblock_3la_2xn_mgj}
    <Error>
      <RequestId>AF55F076-5849-4A53-8844-E25EFBFBD63B</RequestId>
      <HostId>domain.aliyuncs.com</HostId>
      <Code>MissingRegistrantProfileId</Code>
      <Message>RegistrantProfileId is mandatory for this action.</Message>
      <Recommend><![CDATA[https://error-center.aliyun.com/status/search?Keyword=MissingRegistrantProfileId&source=PopGw]]></Recommend>
    </Error>
    ```

-   JSON示例

    ``` {#codeblock_h01_hhi_p9i}
    {
        "Code":"MissingRegistrantProfileId",
        "HostId":"domain.aliyuncs.com",
        "Message":"RegistrantProfileId is mandatory for this action.",
        "Recommend":"https://error-center.aliyun.com/status/search?Keyword=MissingRegistrantProfileId&source=PopGw",
        "RequestId":"ADEEC65F-0AD4-46C0-A518-A3C20A8DBF99"
    }
    ```


## 错误码 {#section_nwb_366_b2b .section}

[单击查看本产品错误码](cn.zh-CN/API 参考/附录/错误代码表.md#)。

