# Sude liche a podobne srandy

Navod pre pocitanie prikladov s pracovnym nazvom "sude-liche". 

**Opisovana metoda ma uspesnost**: ?%

**Vypracoval**: Jakub Jakubec (Kobu#5271)

---

### Intro

Metoda popisuje postupy spominane v [https://is.muni.cz/auth/discussion/predmetove/fi/podzim2019/IB000-14/pomoc_pri_cvicnom_odpovedniku/-/94493426/](https://is.muni.cz/auth/discussion/predmetove/fi/podzim2019/IB000-14/pomoc_pri_cvicnom_odpovedniku/-/94493426/). Takze ak uvidite niekedy pana Darmovzala (viz foto), ktory tuto myslienku prvykrat sformuloval, tak mu podakujte.

![p. Darmovzal kratko po tom ako zapricinil 100% uspesnost tohto prikladu](Sude%20liche%20a%20podobne%20srandy%20c7130d5002b04aad85ec09f8a18480e5/flat750x075f-pad750x1000f8f8f8.jpg)

p. Darmovzal kratko po tom ako zapricinil 100% uspesnost tohto prikladu

Tvorime pravdivostnu tabulku na zaklade uvah, ci nejaky prvok X patri alebo nepatri do danej mnoziny. Takuto tabulku vyhotovime pre lavu (L) a pravu (P) stranu rovnosti, resp. v tabulke bude stlpec $X \in L$ a $X \in R$. Rovnost je platna v pripade ze sa tieto dva stlpce rovnaju*.

### Predpriprava

Na prevod rovnice mnozinoveho kalkulu do vyrokovej formuli pouzijeme nasledujuce vzorce, ktore vyplyvaju jak logicky tak z definic danych operandov.

| Množinový Operand | Formula         |
|-------------------|-----------------|
| A ∩ B             | A ∧ B           |
| A ∪ B             | A ∨ B           |
| A Δ B             | ¬(A <=> B)      |
| A / B             | (A ∧ ¬B)        |

Teraz sa mozme pustit na prvy priklad

### Priklad 1

![pr1.png](Sude%20liche%20a%20podobne%20srandy%20c7130d5002b04aad85ec09f8a18480e5/pr1.png)

Najprv sa za pouzitia asociativity zbavime clenov, ktore prechadzaju cez vsetky i (v tomto pripade len symetricke rozdiely) a vznikne nam takato rovnost:

![new.jpg](Sude%20liche%20a%20podobne%20srandy%20c7130d5002b04aad85ec09f8a18480e5/new.jpg)

Pre citatelnost si vzdy zavediem premenne, ktore budu reprezentovat mnozinu z rovnice.

![pr2.jpg](Sude%20liche%20a%20podobne%20srandy%20c7130d5002b04aad85ec09f8a18480e5/pr2.jpg)

Takze dostavame rovnost:

**$(A - B) \cup ( C Δ B) = (A - C) \cup ( C Δ B)$**

Pomocou uz vyssie spominanych vzorcov zacneme upravovat rovnicu. Budem upravovat max. jeden vyraz z lava do prava  aby bolo vidiet, co sa deje.

$(A ∧¬B) ∪ ( C Δ B) = (A - C) ∪ ( C Δ B)$

$(A ∧¬B) ∨ ( C Δ B) = (A - C) ∪ ( C Δ B)$

$(A ∧¬B) ∨ ¬( C \iff B) = (A - C) ∪ ( C Δ B)$

$(A ∧¬B) ∨ ¬( C \iff B) = (A ∧¬ C) ∪ ( C Δ B)$

$(A ∧¬B) ∨ ¬( C \iff B) = (A ∧¬ C) ∨ ( C Δ B)$

$(A ∧¬B) ∨ ¬( C \iff B) = (A ∧¬ C) ∨ ¬( C \iff B)$

Vsetko mame upravene. Uz len staci **manualne** vyhotovit pravdivostnu tabulku:

![tabulka.png](Sude%20liche%20a%20podobne%20srandy%20c7130d5002b04aad85ec09f8a18480e5/tabulka.png)

A vidime ze P a L sa rovnaju 🙂

### *But wait, there's more

Uvazujme nasledujuci priklad:

![pr3-problem.png](Sude%20liche%20a%20podobne%20srandy%20c7130d5002b04aad85ec09f8a18480e5/pr3-problem.png)

Teraz uz zrychlene ho vyjradrime ako :

$¬(A \iff B) ∧ C = (A ∧¬ (B \iff C)) ∧¬B$ 

V tabulke:

![pr3-problem2.png](Sude%20liche%20a%20podobne%20srandy%20c7130d5002b04aad85ec09f8a18480e5/pr3-problem2.png)

Jednoduche, strany sa nerovnaju!

Lenze odpovednik si mysli inac:

![input.png](Sude%20liche%20a%20podobne%20srandy%20c7130d5002b04aad85ec09f8a18480e5/input.png)

Ako je to mozne ?

### Validita vstupu

Pozrime sa na vstupy predchadzajuceho prikladu, pri ktorych sa strany nerovnali.

A = False
B = True
C = True

Pozrime sa na ake mnoziny tieto premene referovali:

![premenne.jpg](Sude%20liche%20a%20podobne%20srandy%20c7130d5002b04aad85ec09f8a18480e5/premenne.jpg)

Treba sa zamyslet, ci usporiadana trojica (F,T,T) vobec moze nastat → Ak prvok nepatri do zjednotenia vsetkych parnych mnozin, tak urcite nepatri ani do ich symetrickeho rozdielu.

Takychto kontradikcii existuje viacej. Co je treba po kazdom zhotoveni tabulky spravit, je ich ignorovat.

Ak si teda predstavime predoslu tabulku a zbavime sa riadku(ov) s neplatnymi vstupmi dostaneme nasledujuce: 

![pr3-problem2-sol.png](Sude%20liche%20a%20podobne%20srandy%20c7130d5002b04aad85ec09f8a18480e5/pr3-problem2-sol.png)

Teraz si s odpovednikom suhlasime.

Tu su vsetky mozne kontradikcie pri lubovolnom pocte mnozin:

![kontr1.png](Sude%20liche%20a%20podobne%20srandy%20c7130d5002b04aad85ec09f8a18480e5/kontr1.png)

A tu su kontradikcie, ktore nastavaju pri parnom pocte mnozim (to mozme asi ignorovat? 🤷):

![kontr2.png](Sude%20liche%20a%20podobne%20srandy%20c7130d5002b04aad85ec09f8a18480e5/kontr2.png)

### Konec

Niektore kroky su nadbytocne a dali by sa preskocit. Je to na vase uvazenie, tento navod popisuje ako to robim ja.

V pripade najdenych chyb (ci uz logickych alebo gramatickych :D) ma, prosim, kontaktuje na discorde.
