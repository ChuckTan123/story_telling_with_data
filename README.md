# Storytelling With Data Plot Notes

```
Install latex if it isn't available

sudo yum install texlive texlive-latex-extra texlive-fonts-recommended dvipng 
```

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
