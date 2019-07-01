# SaveBatchDomainRemark {#concept_itp_53g_h2b .concept}

SaveBatchDomainRemark：批量保存域名备注。

## 描述 {#section_gtj_vjg_h2b .section}

批量保存域名备注信息。

## 请求参数 {#section_tvx_wjg_h2b .section}

公共请求参数，详见[公共参数](cn.zh-CN/API 参考/调用方式/公共参数.md#)。

|名称|类型|是否必需|描述|
|--|--|----|--|
|Action|String|是|操作接口名，系统规定参数，取值：SaveBatchDomainRemark。|
|Lang|String|否|接口返回信息语言，枚举值范围： -   zh：中文
-   en：英文

 默认为en。|
|InstanceIds|String|是|实例编号列表，建议10条一组，每组最多50条，以逗号“,”隔开。|
|Remark|String|否|备注信息。|

## 返回参数 {#section_uyf_yjg_h2b .section}

|名称|类型|描述|
|--|--|--|
|RequestId|String|唯一请求识别码。|

## 错误码 {#section_zd5_zjg_h2b .section}

|错误代码|描述|HTTP状态码|语义|
|----|--|-------|--|
|ParameterIllegal|Parameter illegal.|400|参数错误。|
|NetworkIOError|Network IO Error.|400|网络I/O异常。|

## 请求示例 {#section_gwx_wjg_h2b .section}

``` {#codeblock_xub_68v_nz0}
http://domain.aliyuncs.com/?Action=SaveBatchDomainRemark
&InstanceId.1=S20182000000000
&InstanceId.2=S20182000000001
&Remark=MyRemarkInfo
&<公共请求参数>
```

## 返回示例 {#section_d2p_2kg_h2b .section}

-   XML示例

    ``` {#codeblock_91e_ff2_f30}
    <?xml version='1.0' encoding='UTF-8'?>
    <SaveBatchDomainRemarkResponse>
        <RequestId>4189E320-961E-4786-8E15-0000</RequestId>
    </SaveBatchDomainRemarkResponse>
    ```

-   JSON示例

    ``` {#codeblock_mr2_uih_2g9}
    {
      "requestId": "F7C66E24-0134-4E53-9A31-0000"
    }
    ```


