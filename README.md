# Storytelling With Data Plot Notes

```
Install latex if it isn't available

sudo yum install texlive texlive-latex-extra texlive-fonts-recommended dvipng 
```

## Bar Plot
<img width="504" alt="Screen Shot 2021-06-08 at 12 15 00 PM" src="https://user-images.githubusercontent.com/29901458/121244007-3b707a80-c853-11eb-814b-30d49c1b86fa.png">
```python
from matplotlib import rc
plt.rcParams.update(
  {
    "text.usetex": True,
    "font.family": "sans-serif",
    "font.sans-serif": ["Helvetica"],
    "figure.dpi": 100
  }
)

# set the color for each bar differently
clrs = ["cornflowerblue" if {some condition} else "grey" for x in column_list ]
sns.barplot(x="x", y="y", data=df, palette=clrs)

# Disable the border of the figure
sns.despine(left = True)

plt.ylabel("Set Y Label")
plt.xlabel("Set X Label")
plt.title("Prefix" + r"\textbf{Being Bold}", loc="left", color="royalblue")
plt.text(10, 0, "Replace the Legend 1", color="darkred")
plt.text(1, 10, "Replace the Legend 2", color="darkred")
plt.text(5, 8, "Additional Info", color="black")
```
