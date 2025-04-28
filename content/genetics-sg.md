
## 🧬 GENETICS EXPLAINED

---

### 🔁 **Genetic Recombination**

| Type                                                                                              | What It Means                                                       | Example                                        |     |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ---------------------------------------------- | --- |
| **Crossing Over**                                                                                 | Recombination between **linked genes** on the same chromosome       | AaBb x aabb → more parentals than recombinants |     |
| **Independent Assortment**                                                                        | Recombination between **unlinked genes** (on different chromosomes) | AaBb x aabb → 1:1:1:1 expected                 |     |
| **More recombinants** = genes are farther apart on a chromosome                                   |                                                                     |                                                |     |
| **Recombination Frequency Formula** = (recombinants ÷ total offspring) × 100 = % or **map units** |                                                                     |                                                |     |

- **Max recombination frequency** = **50%** = unlinked  
- If genes are **linked**, recombination frequency is **<50%**  
- **Parental types = most frequent**  
- **Recombinants = less frequent**

---

### 🔢 **Genotypic vs Phenotypic Ratios**

| Cross Type                       | Genotypic Ratio   | Phenotypic Ratio                 |
| -------------------------------- | ----------------- | -------------------------------- |
| Monohybrid (Aa x Aa)             | 1:2:1 (AA:Aa:aa)  | 3:1 (dom : rec)                  |
| Dihybrid (AaBb x AaBb)           | 1:2:1:2:4:2:1:2:1 | 9:3:3:1                          |
| Incomplete/Codominance (Rr x Rr) | 1:2:1             | 1 red : 2 pink : 1 white         |
| AaBb x aabb (unlinked)           | —                 | 1:1:1:1 (A_B_, A_bb, aaB_, aabb) |

---

### 🧬 **Key Terms**

- **Wild Type** = most common natural phenotype  
- **Barr Body** = inactive X chromosome in females  
- **Hemizygous** = only one allele present (e.g., males for X genes)  
- **Genomic Imprinting** = some genes are silenced based on **parent origin** (epigenetics!)  

---

### 🎲 **Epistasis & Polygenic Traits**

- **Epistasis**: one gene masks another  
  - Example ratio = **9:3:4**  
- **Polygenic Inheritance**: many genes affect one trait  
  - Use formula: **2n + 1 = phenotypes**  
  - Example: skin color, height

---

### ⚖️ **Dominance Types**

| Type | Result |
|------|--------|
| Complete | Dominant masks recessive (Aa = dominant) |
| Incomplete | Blend (Rr = pink from red x white) |
| Codominance | Both show (e.g. AB blood type) |

---

## 👪 PEDIGREE ANALYSIS — HOW TO DETERMINE MODE OF INHERITANCE

---

### Step-by-Step Gameplan:

1. **Does the trait skip generations?**
   - **Yes** → likely **recessive**
   - **No** → likely **dominant**

2. **Are both sexes affected equally?**
   - **Yes** → probably **autosomal**
   - **No (mostly one gender)** → likely **sex-linked**

3. **Are there any carriers?**
   - **Yes = autosomal recessive**
   - **ONLY females can be carriers = sex-linked recessive**

4. **Is every affected daughter’s father also affected?**
   - **Yes** → think **X-linked recessive**

---

### 🎯 Quick Cheat Sheet:

| Inheritance | Key Clues |
|-------------|-----------|
| **Autosomal Dominant** | Trait appears in every generation; both sexes equally; affected parents → affected kids |
| **Autosomal Recessive** | Skips generations; affected kids from unaffected parents; both sexes equally |
| **Sex-Linked Recessive** | Mostly males; skips generations; daughters only affected if dad has it too; mom can be carrier |
| **Sex-Linked Dominant** | No male-to-male transmission; all daughters of affected dads are affected |

---

### 🧬 Barr Bodies

- **One Barr body = 2 X chromosomes**  
- Females = XX (1 Barr body)  
- Males = XY (0 Barr bodies)  
- So: **Yes → 1 Barr body = Female**

---
```mermaid
%% Autosomal Recessive Pedigree Example
graph TD
  %% Generation I
  I1([♂ Unaffected]):::unaffected -->|married| I2([♀ Unaffected]):::unaffected
  
  %% Generation II (Children)
  I1 --> II1([♀ Affected]):::affected
  I2 --> II1
  I1 --> II2([♂ Unaffected]):::unaffected
  I2 --> II2
  I1 --> II3([♂ Unaffected]):::unaffected
  I2 --> II3
  
  %% Generation III (from affected II1)
  II1 --> III1([♂ Unaffected]):::unaffected
  II1 --> III2([♀ Affected]):::affected

  %% Legend
  subgraph Legend [Legend]
    L1([♂ Unaffected]):::unaffected
    L2([♀ Affected]):::affected
  end

  %% Styles
  classDef unaffected fill:#ffffff,stroke:#000000,color:#000000;
  classDef affected fill:#000000,stroke:#000000,color:#ffffff;
  ```

```mermaid
flowchart TD
    %% Nodes
    A[📊 Start: Analyze Pedigree] --> B[Skips generations?]
    
    B -->|Yes| C[Recessive]
    B -->|No| D[Dominant]
    
    C --> E[Affects both sexes equally?]
    D --> F[Affects both sexes equally?]
    
    E -->|Yes| G[Autosomal Recessive]
    E -->|No| H[X-Linked Recessive]
    
    F -->|Yes| I[Autosomal Dominant]
    F -->|No| J[X-Linked Dominant]
    
    H --> K[Only males affected?]
    K -->|Yes| L[X-Linked Recessive]
    K -->|No| M[Recheck Pattern]
    
    J --> N[All daughters of affected dad affected?]
    N -->|Yes| O[X-Linked Dominant]
    N -->|No| P[Recheck Pattern]

    %% Styling
    classDef default fill:#ffffff,stroke:#000000,color:#000000,font-size:12px;
    class A,B,C,D,E,F,G,H,I,J,K,L,M,N,O,P default;

```

