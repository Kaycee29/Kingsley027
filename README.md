- 👋 Hi, I’m Kaycee
- 👀 I’m interested in Data Analytics, Machine learning and project management ...
- 🌱 I’m currently learning DATA analytics...
- 💞️ I’m looking to collaborate on data analytics projects...
- 📫 How to reach me ...

<!---
Kingsley027/Kingsley027 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
Rev_ZeroOrBlank_LatestMonth =
CALCULATE(
    [Revenue],
    FILTER(
        ALLSELECTED('LatestClosedFiscalMonth'),
        'LatestClosedFiscalMonth'[LatestClosedFiscalMonth] = 
            CALCULATE(
                MAX('LatestClosedFiscalMonth'[LatestClosedFiscalMonth])
            ) &&
        (
            [Revenue] = 0 ||
            ISBLANK([Revenue])
        )
    )
)
