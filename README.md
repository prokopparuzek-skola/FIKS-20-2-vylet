# Výlet

Rozdělím si případy které mohou nastat na dvě části.

1) Nejlepší možné řešení obsahuje alespoň polovinu všech dveří

Algoritmus určitě není více než dvakrát horší než nejlepší možné řešení, protože i kdybych na seznam zařadil všechny 
dveře stále to bude maximálně dvakrát více než je minimální počet dveří na seznamu.\
2) Nejlepší možné řešení je menší než polovina všech dveří

Pak zaručeně musí existovat alespoň dva světy se společným východem. Kdyby měl každý svět svůj vlastní vchod i východ, 
bude minimální možné řešení obsahovat polovinu všech dveří, pokud by nějaké světy měli společný vchod, tak bude nejmenší 
řešení určitě obsahovat více dveří než polovinu, východů je více než vchodů. Abych zmenšil nejmenší řešení pod polovinu 
musím spojit východy z více světů do jednoho.

V případě kdyby každý svět měl svůj vchod, který zároveň nefiguruje, jako východ, což je nejhorší možný případ, jelikož 
algoritmus do seznamu zahrne mnoho zbytečných dveří, konkrétně nejvyšší možný počet. Tak na každý východ, který spojím, 
algoritmus odstraní jeden vchod, druhý napojený svět vyškrtne a nezapočítá jeho vchod.

Takže v nejhorší možném případě, tj. každý svět má svůj vchod a východ, kde spojím několik východů, je nejlepší řešení 
rovné počtu východů. Algoritmus v tomto případě zařadí na seznam všechny východy a od celkového počtu vchodů odečte 
rozdíl mezi počtem vchodů a východů a ten přičte. Takže zařadí stejně vchodů jako východů a to je přesně dvojnásobek 
minimálního možného řešení.

V případě, že by byly spojené vchody, algoritmus zařadí méně vchodů a tím páde bude celkový počet dveří ještě menší než 
dvojnásobek minimálního. V případě více spojených východů to platí obdobně.
