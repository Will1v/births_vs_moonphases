# Requirements

**Libraries:**

- Pandas: `pip install pandas`
- matplotlib: `python -m pip install -U matplotlib`
- plotly: `pip install plotly`

**Raw data:**

- US daily births, from 2000 to 2014: https://www.kaggle.com/datasets/mysarahmadbhat/us-births-2000-to-2014
- Full moon dates, from 1900 to 2050: https://www.kaggle.com/datasets/lsind18/full-moon-calendar-1900-205

# Context

There is a strong belief among hospital staff that full moon nights are busier because of more women giving birth on these nights.

# Objective

This is an attempt to see if there is any correlation (not necessarily causality) between the two.

**Nota Bene**: to access the dynamic charts, download and run the [Jupyter notebook](https://github.com/Will1v/births_vs_moonphases/blob/main/births_v_moon_cycles.ipynb).

# Analysis

## Week days vs weekends

At first glance, there seem to be two (if not three) groups of points:

![image](https://github.com/user-attachments/assets/c521bb55-3676-426d-ae7a-6c341ecf4933)

An intuition would be that the 2 lower groups may be weekends (Sundays being the lowest) because of fewer induced births happen on these days (hospitals being more lightly staffed).
Plotting weekends in a different colour confirms that intuition:

![image](https://github.com/user-attachments/assets/563de03d-58af-4fa9-aa9d-ffa008161559)

## Rolling averages

Let's look at rolling averages on the full data set vs full moon days only.

We are going to take 90 days sliding windows to compare all regular days vs full moon only days. 
Given moon cycles are about 29.5 days long, I've used 3 days as a sliding window in the full moon days df ($3 * 29.5 \approx 90$).

![image](https://github.com/user-attachments/assets/646a9c55-d492-4625-a157-4ff6d289eca2)

Full moon birth counts seem to be homogeneously distributed.

## Yearly breakdown

To confirm, let's breakdown average birth counts year by year

![image](https://github.com/user-attachments/assets/9b78af29-0dde-43b2-bbfd-008f3d952763)

# Conclusion

Based on US births from 2000 to 2014, there doesn't seem to be any particular correlation between full moon days and birth counts.
