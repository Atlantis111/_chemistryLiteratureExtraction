# 基于MaterialsBert和MoonshotAI(月之暗面)的文献实体属性提取系统

## 程序功能
文献分段，存放，使用BERT进行语义预处理，再调用MoonShot AI大模型进行文献提取，输出json格式三元组(实体-属性名-属性值，例如NF90，温度，100S℃)
结果导出至excel中
构建了本地知识库，加入了检索增强RAG；
构建了少样本下游微调训练，让LLM输出符合三元组格式
推理结果后处理，加入了实体名合理性检测，单位统一

## 程序默认提取属性表如下：
提取结果存放至PostgreSQL数据库中：
1	温度	Temperature

2	水通量	Water Flux

3	脱盐率 / 截留率	Salt Rejection / Removal Rate

4	操作压力	Operating Pressure

5	回收率	Recovery Rate

6	膜孔径	Membrane Pore Size

7	接触角	Contact Angle

8	表面粗糙度	Surface Roughness

9	Zeta电位	Zeta Potential

10	孔隙率	Porosity

11	机械强度	Mechanical Strength

12	耐氯/抗氧化性	Chlorine / Oxidant Resistance

13	适用的pH范围	Applicable pH Range

14	截留分子量	Molecular Weight Cut-Off (MWCO)

15	平均水通量	Average Permeate Flux

16	通量衰减率	Flux Decline Rate

17	接触角滞后	Contact Angle Hysteresis

18	表面能	Surface Energy

19	耐污染性	Fouling Resistance

20	化学稳定性	Chemical Stability

## 推理结果
实体名表：
<img width="1163" height="310" alt="image" src="https://github.com/user-attachments/assets/678f338f-4fed-4178-a40d-1abd0b6a5451" />

属性名，属性值表：
<img width="1734" height="342" alt="image" src="https://github.com/user-attachments/assets/89676075-f84f-480e-9fae-f86fda5d608c" />
