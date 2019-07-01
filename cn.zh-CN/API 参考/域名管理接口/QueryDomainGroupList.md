# QueryDomainGroupList {#concept_t5n_hhm_c2b .concept}

QueryDomainGroupList：查询域名分组列表。

## 请求参数 {#section_nnf_shm_c2b .section}

|参数|类型|是否必选|示例值|描述|
|:-|:-|:---|:--|:-|
|DomainGroupName|String|否|默认分组|域名分组名称。|
|Lang|String|否|en|接口返回错误信息语言，枚举值范围：zh 中文；en 英文。默认为 en。|
|ShowDeletingGroup|Boolean|否|false|是否展示正在删除中的域名分组，默认为false。|
|UserClientIp|String|否|127.0.0.1|用户IP。|

## 返回参数 {#section_yqn_vhm_c2b .section}

|参数|类型|示例值|描述|
|:-|:-|:--|:-|
|RequestId|String|80011ABC-F573-4795-B0E8-377BFBBA3422|唯一请求标识码。|
|Data| | |域名分组列表。|
|└DomainGroupId|String|-1|域名分组编号。|
|└DomainGroupName|String|未分组|域名分组名称。|
|└TotalNumber|Integer|20|域名数量。|
|└CreationDate|String|2018-04-02 15:59:06|域名分组创建时间。|
|└ModificationDate|String|2018-04-02 15:59:06|域名分组修改时间。|
|└DomainGroupStatus|String|COMPLETE|域名分组状态。枚举值范围： -   PROCESSING 处理中
-   COMPLETE 已完成

 **说明：** ：通过文件设置分组、替换超过1,000个域名的分组等情况为异步过程，需要等待系统处理，此状态下该字段为PROCESSING。

 |
|└BeingDeleted|Boolean|false|是否正在删除中。 **说明：** 超过1,000个域名的分组删除为异步过程，需要系统处理一段时间，在此期间内该字段为true。

 |

## 示例 {#section_of5_382_b2b .section}

**请求示例**

``` {#codeblock_zaq_udv_144}
/?Action=QueryDomainGroupList
&DomainGroupName=默认分组
&<公共请求参数>
```

**正常返回示例**

-   XML示例

    ``` {#codeblock_fmd_3xc_e41}
    <QueryDomainGroupListResponse>
      <Data>
        <DomainGroup>
          <DomainGroupId>-1</DomainGroupId>
          <BeingDeleted>false</BeingDeleted>
          <DomainGroupName>未分组</DomainGroupName>
          <CreationDate>2018-04-27 14:49:10</CreationDate>
          <TotalNumber>346</TotalNumber>
          <DomainGroupStatus>COMPLETE</DomainGroupStatus>
       </DomainGroup>
      </Data>
      <RequestId>AA897378-08E9-4C34-98F9-8689F4EDC98E</RequestId>
    </QueryDomainGroupListResponse>
    ```

-   JSON示例

    ``` {#codeblock_lk6_yr1_p59}
    {
        "Data":{
            "DomainGroup":[{
                "BeingDeleted":false,
                "CreationDate":"2018-04-27 14:48:02",
                "DomainGroupId":-1,
                "DomainGroupName":"未分组",
                "DomainGroupStatus":"COMPLETE",
                "TotalNumber":346
            }]
        },
        "RequestId":"49F5586F-4D94-4909-8C6F-7DD5072ED08D"
    }
    ```


**异常返回示例**

-   XML示例

    ``` {#codeblock_ezv_2uf_ia7}
    <Error>
      <RequestId>F0B47FE6-C774-4833-9028-B073588A8FAA</RequestId>
      <Code>InternalError</Code>
      <Message>The request processing has failed due to some unknown error, exception or failure</Message>
    </Error>
    ```

-   JSON示例

    ``` {#codeblock_bir_fr7_huy}
    {
        "Code":"InternalError",
        "Message":"The request processing has failed due to some unknown error, exception or failure",
        "RequestId":"E246E023-F2EB-4034-83F7-B13FCF31459C"
    }
    ```


## 错误码 {#section_nwb_382_b2b .section}

[单击查看本产品错误码](cn.zh-CN/API 参考/附录/错误代码表.md#)。

