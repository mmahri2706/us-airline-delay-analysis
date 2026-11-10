# Dataset setup

This repository does **not** include the processed data file required to rerun the notebook.

Place the previously cleaned BTS workbook in the repository root with the exact filename:

```text
BTS_top20_airline.xlsx
```

The notebook loads it using `pd.read_excel("BTS_top20_airline.xlsx")`.

The report states that the dataset contains **13,472 records and 25 columns** from **20 selected U.S. airports**, covering January 2022 through July 2026. This is a description from the notebook and has not been independently revalidated here.

Fields referenced in the analysis include:

- `year`, `month`, `carrier`, `carrier_name`, `airport`
- `arr_flights`, `arr_del15`, `arr_delay`, `delay_rate`, `minutes_per_delayed_flight`, `low_sample_flag`
- Delay cause counts: `carrier_ct`, `weather_ct`, `nas_ct`, `security_ct`, `late_aircraft_ct`
- Delay cause minutes: `carrier_delay`, `weather_delay`, `nas_delay`, `security_delay`, `late_aircraft_delay`

Raw data can be explored at [BTS TranStats](https://www.transtats.bts.gov/), but raw exports are **not** direct replacements for this workbook. The cleaned data pipeline is not part of the uploaded notebook.

The `.gitignore` intentionally excludes Excel/CSV data files, to avoid accidentally uploading local or unreviewed datasets. If you own redistribution rights and want to publish the processed data, review provenance and applicable terms before selectively adding the file.
