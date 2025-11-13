# 📊 Bank Marketing Dataset — Summary

**Source:** UCI Machine Learning Repository  
**Purpose:** Predict whether a client will subscribe to a **term deposit** (`y`) based on demographic and marketing-campaign features.  
**Instances:** 45,211  
**Features:** 16 (categorical + numeric)  
**Target:** `y` (yes/no)  
**Missing Values:** Yes (`NaN`)  
**Year:** 2014  
**Creators:** S. Moro, P. Rita, P. Cortez

---

## 📁 Dataset Description

The dataset contains records from direct marketing campaigns (phone calls) conducted by a Portuguese bank.  
Often multiple calls were needed to determine customer interest in a term deposit.

---

## 🧾 Variable Dictionary

### 🧑‍💼 1. **Client Attributes**
| Variable | Type | Meaning |
|---------|------|---------|
| **age** | numeric | Client's age |
| **job** | categorical | Type of job (e.g., admin., technician, retired, student, etc.) |
| **marital** | categorical | Marital status: married, divorced/widowed, single |
| **education** | categorical | Education level: primary, secondary, tertiary, unknown |
| **default** | binary | Has credit in default? |
| **balance** | numeric | Yearly average account balance (in euros) |
| **housing** | binary | Has a housing loan? |
| **loan** | binary | Has a personal loan? |

### ☎️ 2. **Last Contact of Current Campaign**
| Variable | Type | Meaning |
|---------|------|---------|
| **contact** | categorical | Communication type: cellular, telephone, unknown |
| **day** | numeric | Day of month of last contact |
| **month** | categorical | Month of last contact (jan–dec) |
| **duration** | numeric | Last call duration (seconds) |

### 📞 3. **Campaign History**
| Variable | Type | Meaning |
|---------|------|---------|
| **campaign** | numeric | Number of contacts in this campaign (including last one) |
| **pdays** | numeric | Days since last contact in previous campaign (−1 = never contacted) |
| **previous** | numeric | Number of contacts prior to this campaign |
| **poutcome** | categorical | Outcome of previous campaign: success, failure, other, unknown |

### 🎯 4. **Target Variable**
| Variable | Type | Meaning |
|---------|------|---------|
| **y** | binary | Did the client subscribe a term deposit? (yes/no) |

---

## 🔍 Task Type
- **Supervised Classification**  
- Predictive target: **Subscription to term deposit (y)**

---

## 📑 Reference Paper
**A data-driven approach to predict the success of bank telemarketing**  
*Moro, Cortez, Rita — Decision Support Systems (2014)*  
DOI: 10.1016/j.dss.2014.03.001


# 🔢 Categorical Value Counts by Variable Group

---

## 🧑‍💼 1. Client Attributes

### **job**
| Job Category      | Count |
|-------------------|-------|
| blue-collar       | 9732  |
| management        | 9458  |
| technician        | 7597  |
| admin.            | 5171  |
| services          | 4154  |
| retired           | 2264  |
| self-employed     | 1579  |
| entrepreneur      | 1487  |
| unemployed        | 1303  |
| housemaid         | 1240  |
| student           | 938   |
| Not Specified     | 288   |

---

### **marital**
| Marital Status | Count |
|----------------|-------|
| married        | 27214 |
| single         | 12790 |
| divorced       | 5207  |

---

### **education**
| Education Level | Count |
|-----------------|-------|
| secondary       | 23202 |
| tertiary        | 13301 |
| primary         | 6851  |
| Not Specified   | 1857  |

---

### **default**
| Default | Count |
|---------|-------|
| no      | 44396 |
| yes     | 815   |

---

### **housing**
| Housing Loan | Count |
|--------------|-------|
| yes          | 25130 |
| no           | 20081 |

---

### **loan**
| Personal Loan | Count |
|---------------|-------|
| no            | 37967 |
| yes           | 7244  |

---

## ☎️ 2. Last Contact of Current Campaign

### **contact**
| Contact Type | Count |
|--------------|-------|
| cellular     | 29285 |
| Not Specified| 13020 |
| telephone    | 2906  |

---

### **month**
| Month | Count |
|-------|-------|
| may   | 13766 |
| jul   | 6895  |
| aug   | 6247  |
| jun   | 5341  |
| nov   | 3970  |
| apr   | 2932  |
| feb   | 2649  |
| jan   | 1403  |
| oct   | 738   |
| sep   | 579   |
| mar   | 477   |
| dec   | 214   |

---

## 📞 3. Campaign History

### **poutcome**
| Previous Outcome | Count |
|------------------|-------|
| Not Specified    | 36959 |
| failure          | 4901  |
| other            | 1840  |
| success          | 1511  |

---

## 🎯 4. Target Variable

### **y**
| Subscription | Count |
|--------------|-------|
| no           | 39922 |
| yes          | 5289  |

---

# 📈 Numerical Variable Summary

| Statistic |   age    |   balance    | duration  | campaign |  pdays   | previous |
|-----------|----------|--------------|-----------|----------|----------|----------|
| **mean**  | 40.93621 | 1362.272058  | 258.16308 | 2.763841 | 40.197828| 0.580323 |
| **std**   | 10.618762| 3044.765829  | 257.527812| 3.098021 |100.128746| 2.303441 |
| **min**   | 18.0     | -8019.0      | 0.0       | 1.0      | -1.0     | 0.0      |
| **25%**   | 33.0     | 72.0         | 103.0     | 1.0      | -1.0     | 0.0      |
| **50%**   | 39.0     | 448.0        | 180.0     | 2.0      | -1.0     | 0.0      |
| **75%**   | 48.0     | 1428.0       | 319.0     | 3.0      | -1.0     | 0.0      |
| **max**   | 95.0     | 102127.0     | 4918.0    | 63.0     | 871.0    | 275.0    |

---

# 🔝 Models Ranked by Recall — Highest to Lowest

| Rank | Model               | Recall      | Precision      | F1     | Accuracy | ROC AUC |
|------|---------------------|-------------|----------------|--------|----------|---------|
| 1    | Logistic Regression | **0.612**   | 0.273          | 0.378  | 0.764    | 0.7635  |
| 2    | Decision Tree       | **0.579**   | 0.252          | 0.351  | 0.749    | 0.7251  |
| 3    | Naive Bayes         | 0.290       | 0.528          | 0.374  | 0.887    | 0.7498  |
| 4    | EBM                 | 0.181       | 0.650          | 0.283  | 0.893    | 0.7781  |
