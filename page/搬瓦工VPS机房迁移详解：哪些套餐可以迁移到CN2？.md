# 搬瓦工VPS机房迁移详解：哪些套餐可以迁移到CN2？

关于搬瓦工VPS的机房迁移问题，不少用户关心自己的套餐是否支持机房迁移，能否迁移到CN2线路，迁移后的流量是否会发生变化。本文将为您详细解答这些问题。

👉 [【建议收藏】2025年搬瓦工最新优惠套餐整理汇总 - 每日更新最新可用优惠码](https://bit.ly/banwagon)

## 哪些套餐可以迁移？

并非所有搬瓦工的套餐都支持机房迁移。以下套餐 **不支持机房迁移**：

- **SPECIAL 10G KVM PROMO V3 – LOS ANGELES – CHINA DIRECT ROUTE** （仅限QNET）
- **SPECIAL 20G KVM PROMO V3 – LOS ANGELES – CHINA DIRECT ROUTE** （仅限QNET）
- **SPECIAL 10G VZ PROMO V3 – LOS ANGELES – CHINA DIRECT ROUTE** （仅限QNET）
- **SPECIAL 20G VZ PROMO V3 – LOS ANGELES – CHINA DIRECT ROUTE** （仅限QNET）
- **SPECIAL 10G VZ PROMO V3 – FREMONT CA** （仅限弗里蒙特）
- **SPECIAL 20G VZ PROMO V3 – FREMONT CA** （仅限弗里蒙特）

此外，一些过期的套餐（例如，限定凤凰城的11.99套餐）同样不支持迁移。

**除了上述限制套餐以外，其他搬瓦工套餐均支持机房迁移**。

## 可迁移的机房列表

### KVM版支持迁移的机房（共8个）

- **USA West coast (California – Los Angeles DC8 CN2)** 洛杉矶
- **USA West coast (California – Los Angeles DC3 CN2)** 洛杉矶（新增）
- USA West coast (California – Los Angeles DC2 QNET) 洛杉矶
- USA West coast (California – Los Angeles DC4 MCOM) 洛杉矶
- USA West coast (California – Fremont) 弗里蒙特
- USA East coast (New York) 纽约
- Canada, Vancouver 加拿大 温哥华
- EU (Netherlands) 荷兰

### OVZ版支持迁移的机房（共7个）

- USA East coast (New York) 纽约
- USA West coast (California – Los Angeles DC2 QNET) 洛杉矶
- USA West coast (California – Los Angeles DC4 MCOM) 洛杉矶
- USA West coast (California – Fremont) 弗里蒙特
- **USA West coast (Phoenix Arizona)** 凤凰城
- EU (Netherlands) 荷兰
- Canada, Vancouver 加拿大 温哥华

**区别总结**：

- **KVM版**：支持迁移到CN2机房。
- **OVZ版**：不支持迁移到CN2机房，但可以选择迁到凤凰城机房。

## CN2新机房说明

从2017年11月14日起，搬瓦工新增了一个CN2机房：

- **DC8**：C3机房的CN2线路
- **DC3**：QN机房的CN2线路

用户可以根据测试IP的实际表现自行选择合适的机房型号。

## 迁移到CN2后流量会如何变化？

- **常规KVM版套餐**：迁移到CN2后，流量额度会减少至原来的 **三分之一**。
- **CN2 KVM版套餐**：迁移到其他机房，流量额度保持不变。

迁移前，请务必确认自己的流量使用需求，以选择合适的机房和线路。

---

通过以上信息，相信您对于搬瓦工VPS的机房迁移支持情况已经有了清晰的了解。如果您有更多疑问，请通过测试和实际需求，选择最适合您的迁移方案。