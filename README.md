<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=IBM+Plex+Mono&size=28&duration=2500&pause=800&color=B5651D&center=true&vCenter=true&width=650&lines=Oil+Recovery+Register;Transformer+Repair+%26+DTC+Ledger;Synced+Live+to+Google+Sheets" alt="Typing SVG" />

<br>

![Made with HTML](https://img.shields.io/badge/Frontend-HTML%2FJS-1b3a4b?style=for-the-badge)
![Google Apps Script](https://img.shields.io/badge/Backend-Google%20Apps%20Script-b5651d?style=for-the-badge&logo=google)
![Google Sheets](https://img.shields.io/badge/Storage-Google%20Sheets-2f6b5e?style=for-the-badge&logo=googlesheets&logoColor=white)
![Status](https://img.shields.io/badge/status-active-brightgreen?style=for-the-badge)

<img src="https://user-images.githubusercontent.com/74038190/212284100-561aa473-3905-4a80-b561-0d28506553ee.gif" width="500">

</div>

---

## 📋 About

**Oil Recovery Register** ek single-file web app hai jo Electricity Workshop Centres (AZAMGARH, MAU, BALLIA, EWD) ke liye:

- 🔧 Transformer **Repair** aur **DTC** data monthly entry
- 🛢️ **Oil Balance** tracking (Fresh Oil, B&C Oil, Reclaim Oil, O&U)
- 📊 Custom date-range **Summary Reports** (Opening balance hamesha "From Month" se)
- 📥 One-click **Excel export** — original template format me
- ☁️ Har entry seedha **aapki Google Sheet** me chronological order me save hoti hai

<div align="center">
<img src="https://user-images.githubusercontent.com/74038190/213910845-af37a709-8995-40d6-b0ad-07486b380c9e.gif" width="500">
</div>

---

## ⚙️ How it works

```mermaid
flowchart LR
    A["🖥️ oil_recovery_app.html"] -- "fetch() POST" --> B["📜 Code.gs (Apps Script Web App)"]
    B -- "reads / writes rows" --> C["📊 Google Sheet"]
    C -- "chronological blocks" --> D["AZAMGARH · MAU · BALLIA · EWD"]
```

1. `oil_recovery_app.html` browser me khulti hai — koi install nahi chahiye
2. Data entry form se values Apps Script Web App ko bheji jaati hain
3. `Code.gs` sahi centre ke sheet-tab me sahi jagah (month order maintain karke) block insert/update karti hai
4. Summary tab se kisi bhi date range ka report Excel me download ho sakta hai

---

## 🚀 Setup

1. Apni Google Sheet kholo → **Extensions → Apps Script**
2. `Code.gs` ka poora content paste karo
3. **Deploy → New deployment → Web app**
   - Execute as: **Me**
   - Who has access: **Anyone**
4. Mile hue `.../exec` URL ko copy karo
5. `oil_recovery_app.html` kholo → **Google Sheet Sync** box me URL paste karo → **Save & Connect**

<div align="center">
<img src="https://user-images.githubusercontent.com/74038190/216122041-518ac897-8d92-4c6b-9b3f-ca01dcaf38ee.png" width="60">
</div>

---

## 📁 Files

| File | Kaam |
|---|---|
| `oil_recovery_app.html` | Poora frontend app — data entry + summary + Excel export |
| `Code.gs` | Google Apps Script backend — Sheet ke saath read/write bridge |

---

<div align="center">

**Made for PUVVNL Electricity Workshop Centres**

<img src="https://user-images.githubusercontent.com/74038190/212284158-e840e285-664b-44d7-b79b-e264b5030eb4.gif" width="100">

</div>
