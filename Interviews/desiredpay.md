# Desired Pay (What is my Actual Inome if I ask for a certain income?)

## One Tax Bracket

$$ ActualIncome = \frac{AskedIncome}{1-TaxRate} $$

## Multiple Tax Brackets

$$ ActualIncome = \frac{AskedIncome-BottomOfClosestIncomeBracket}{1-TaxRate} + \sum_i^N Spread_iTR_i $$
where
$$ Spread_i  =  Diff between i_{th} top and bottom of tax bracket $$
$$ TR_i is the Tax rate of the i_{th} tax bracket$$
