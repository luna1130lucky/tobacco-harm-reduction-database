# 字段说明

- `companies.csv`：公司索引。company_id、公司名称、总部、官网与备注。
- `brands.csv`：品牌索引。brand_id 通过 company_id 关联公司。
- `products.csv`：产品规格。按“型号 × 口味 × 尼古丁含量 × 市场版本”建档，设备与烟支/烟弹分开。口含烟下区分含烟叶的口腔烟草和不含烟叶的尼古丁袋。
- `markets.csv`：市场记录。record_type 使用 Launch、Announced launch、Regulatory scope、Observed availability；监管管辖区不代表实际销售。date_precision 使用 year、month、day。
- `prices.csv`：价格快照。price、currency、pack_quantity、pack_unit、country、city、retailer、sales_location、price_type、tax_included、price_date、observed_at 必须一起理解；历史官方定价不是当前售价。
- `pmta.csv`：FDA 证据。status 使用 Authorized、Historical MGO、Pending、Denied、Withdrawn、Revoked。Unrecorded 由网页在没有记录时生成，不是 FDA 审核结论。mrtp_status、mrtp_date、mrtp_source_url 单独记录 MRTP。
- 所有表保留 source、source_url 和 last_updated/verified_at。每次状态变化新增记录，保留历史。

主要来源：[FDA 尼古丁袋当前清单](https://www.fda.gov/tobacco-products/market-and-distribute-tobacco-product/nicotine-pouch-products-authorized-fda)、[FDA 电子烟当前清单](https://www.fda.gov/tobacco-products/market-and-distribute-tobacco-product/e-cigarettes-vapes-and-other-electronic-nicotine-delivery-systems-ends-authorized-fda)、[FDA 历史 MGO 表](https://www.fda.gov/tobacco-products/premarket-tobacco-product-applications/premarket-tobacco-product-marketing-granted-orders)、[JT Ploom AURA 新闻稿](https://www.jt.com/media/news/2025/0527_E01.html)、[The Korea Times lil AIBLE 报道](https://www.koreatimes.co.kr/business/companies/20221109/ktg-launches-new-hnb-lil-aible)。
