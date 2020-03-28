[node-expose-sspi](../README.md) › ["lib/adsi.d"](../modules/_lib_adsi_d_.md) › [IDirectorySearch](_lib_adsi_d_.idirectorysearch.md)

# Interface: IDirectorySearch

## Hierarchy

* [IID](_lib_adsi_d_.iid.md)

  ↳ **IDirectorySearch**

## Index

### Methods

* [ExecuteSearch](_lib_adsi_d_.idirectorysearch.md#executesearch)
* [GetColumn](_lib_adsi_d_.idirectorysearch.md#getcolumn)
* [GetNextColumnName](_lib_adsi_d_.idirectorysearch.md#getnextcolumnname)
* [GetNextRow](_lib_adsi_d_.idirectorysearch.md#getnextrow)
* [Release](_lib_adsi_d_.idirectorysearch.md#release)
* [SetSearchPreference](_lib_adsi_d_.idirectorysearch.md#setsearchpreference)

## Methods

###  ExecuteSearch

▸ **ExecuteSearch**(`input`: object): *void*

*Defined in [lib/adsi.d.ts:14](https://github.com/jlguenego/node-expose-sspi/blob/e275dcb/lib/adsi.d.ts#L14)*

**Parameters:**

▪ **input**: *object*

Name | Type |
------ | ------ |
`filter` | string |

**Returns:** *void*

___

###  GetColumn

▸ **GetColumn**(`colName`: string): *string | number | false | true[]*

*Defined in [lib/adsi.d.ts:17](https://github.com/jlguenego/node-expose-sspi/blob/e275dcb/lib/adsi.d.ts#L17)*

**Parameters:**

Name | Type |
------ | ------ |
`colName` | string |

**Returns:** *string | number | false | true[]*

___

###  GetNextColumnName

▸ **GetNextColumnName**(): *string | [HRESULT](../modules/_lib_adsi_d_.md#hresult)*

*Defined in [lib/adsi.d.ts:16](https://github.com/jlguenego/node-expose-sspi/blob/e275dcb/lib/adsi.d.ts#L16)*

**Returns:** *string | [HRESULT](../modules/_lib_adsi_d_.md#hresult)*

___

###  GetNextRow

▸ **GetNextRow**(): *[HRESULT](../modules/_lib_adsi_d_.md#hresult)*

*Defined in [lib/adsi.d.ts:15](https://github.com/jlguenego/node-expose-sspi/blob/e275dcb/lib/adsi.d.ts#L15)*

**Returns:** *[HRESULT](../modules/_lib_adsi_d_.md#hresult)*

___

###  Release

▸ **Release**(): *void*

*Inherited from [IID](_lib_adsi_d_.iid.md).[Release](_lib_adsi_d_.iid.md#release)*

*Defined in [lib/adsi.d.ts:4](https://github.com/jlguenego/node-expose-sspi/blob/e275dcb/lib/adsi.d.ts#L4)*

**Returns:** *void*

___

###  SetSearchPreference

▸ **SetSearchPreference**(): *void*

*Defined in [lib/adsi.d.ts:13](https://github.com/jlguenego/node-expose-sspi/blob/e275dcb/lib/adsi.d.ts#L13)*

**Returns:** *void*