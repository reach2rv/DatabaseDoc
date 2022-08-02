

# ![logo](../../../../../Images/table64.svg) dbo.ApprovalPurchase

## <a name="#Description"></a>Description
> 
## <a name="#Columns"></a>Columns
|Key|Name|Data Type|Length|Precision|Scale|Not Null|Identity|Rule|Default|Computed|Persisted|Description|
|:---:|---|---|---|---|---|---|---|---|---|---|---|---|
|[![Primary Key PK_ApprovalPurchase](../../../../../Images/primarykey.svg)](#Indexes)[![Cluster Key PK_ApprovalPurchase](../../../../../Images/Cluster.svg)](#Indexes)|TransId|bigint|8|19|0|True|1 - 1|||False|False||
||TransDate|datetime2|8|27|7|True||||False|False||
||VoucherNo|varchar|100|0|0|True||||False|False||
||VoucherTypeId|int|4|10|0|False||||False|False||
||DepartmentId|int|4|10|0|False||||False|False||
||PartyId|int|4|10|0|False||||False|False||
||BaseItemTypeId|int|4|10|0|False||||False|False||
||TermsId|int|4|10|0|False||||False|False||
||CurrencyId|int|4|10|0|False||||False|False||
||ExchRate|numeric|9|18|3|False||||False|False||
||NetAmount|numeric|13|20|2|False||||False|False||
||Roundoff|numeric|13|20|2|False||||False|False||
||TaxAmount|numeric|13|20|2|False||||False|False||
||Discount|numeric|13|20|2|False||||False|False||
||AdditionalCharges|numeric|13|20|2|False||||False|False||
||GrossAmount|numeric|13|20|2|False||||False|False||
||CCNetAmount|decimal|13|20|2|False|||(0)|False|False||
||CCGrossAmount|numeric|13|20|2|False|||(0)|False|False||
||Pieces|int|4|10|0|False||||False|False||
||Weight|decimal|13|20|3|False||||False|False||
||NetWeight|decimal|13|20|3|False||||False|False||
||Remark|varchar||0|0|False||||False|False||
||CompanyId|int|4|10|0|False||||False|False||
||BillNo|varchar|50|0|0|False||||False|False||
||BillDate|datetime2|8|27|7|False||||False|False||
||ChallanNo|varchar|50|0|0|False||||False|False||
||ChallanDate|datetime2|8|27|7|False||||False|False||
||EmployeeId|int|4|10|0|False||||False|False||
||AddressId|int|4|10|0|False||||False|False||
||ShipmentId|int|4|10|0|False||||False|False||
||ShipAddressId|int|4|10|0|False||||False|False||
||FinancialYearId|int|4|10|0|False||||False|False||
||UserId|int|4|10|0|False||||False|False||
||RefTransId|bigint|8|19|0|False||||False|False||
||RefVoucherId|int|4|10|0|False||||False|False||
||IsPosted|bit|1|1|0|False||||False|False||
||PostingDate|datetime2|8|27|7|False||||False|False||

## <a name="#Indexes"></a>Indexes
|Key|Name|Columns|Unique|Type|Description|
|:---:|---|---|---|---|---|
|[![Primary Key PK_ApprovalPurchase](../../../../../Images/primarykey.svg)](#Indexes)[![Cluster Key PK_ApprovalPurchase](../../../../../Images/Cluster.svg)](#Indexes)|PK_ApprovalPurchase|TransId|True|||

## <a name="#SqlScript"></a>SQL Script
```SQL
CREATE TABLE dbo.ApprovalPurchase (
  TransId bigint IDENTITY,
  TransDate datetime2 NOT NULL,
  VoucherNo varchar(100) NOT NULL,
  VoucherTypeId int NULL,
  DepartmentId int NULL,
  PartyId int NULL,
  BaseItemTypeId int NULL,
  TermsId int NULL,
  CurrencyId int NULL,
  ExchRate numeric(18, 3) NULL,
  NetAmount numeric(20, 2) NULL,
  Roundoff numeric(20, 2) NULL,
  TaxAmount numeric(20, 2) NULL,
  Discount numeric(20, 2) NULL,
  AdditionalCharges numeric(20, 2) NULL,
  GrossAmount numeric(20, 2) NULL,
  CCNetAmount decimal(20, 2) NULL DEFAULT (0),
  CCGrossAmount numeric(20, 2) NULL DEFAULT (0),
  Pieces int NULL,
  Weight decimal(20, 3) NULL,
  NetWeight decimal(20, 3) NULL,
  Remark varchar(max) NULL,
  CompanyId int NULL,
  BillNo varchar(50) NULL,
  BillDate datetime2 NULL,
  ChallanNo varchar(50) NULL,
  ChallanDate datetime2 NULL,
  EmployeeId int NULL,
  AddressId int NULL,
  ShipmentId int NULL,
  ShipAddressId int NULL,
  FinancialYearId int NULL,
  UserId int NULL,
  RefTransId bigint NULL,
  RefVoucherId int NULL,
  IsPosted bit NULL,
  PostingDate datetime2 NULL,
  CONSTRAINT PK_ApprovalPurchase PRIMARY KEY CLUSTERED (TransId)
)
ON [PRIMARY]
TEXTIMAGE_ON [PRIMARY]
GO
```

## <a name="#DependsOn"></a>Depends On _`1`_
- ![Database](../../../../../Images/database.svg) TabAurous_Dev


## <a name="#UsedBy"></a>Used By
No items found

||||
|---|---|---|
|Author: Arvind Sawant|Copyright © GreySauce Technologies All Rights Reserved|Created: 02-08-2022|