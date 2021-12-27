# Undroppable Table

The document contains no text but it does have 8 columns of coloured boxes. This hints at it being ASCII, with no cell background being 0s and blue cells being 1s. Create a function to determine if a cell is blank or blue using VBA. Use `Alt + F11` to open VPA and then `F5` to create a function called "InteriorColor":

```vba
Function InteriorColor(CellColor As Range)
Application.Volatile
InteriorColor = CellColor.Interior.ColorIndex
End Function
```

[Reference](https://techcommunity.microsoft.com/t5/excel/formula-or-function-for-if-statement-based-on-cell-color/m-p/78267)

Working in adjacent cells J to Q, put the formula `=InteriorColor(A1)` into J1. Copy and paste the formula for row 1 by dragging the cell. In the next adjacent cell S1, put the formula `=IF(J1=-4142,0,128)`. Copy and paste this formula for columns S - Z. For each cell, change the value of the last paramater to match the corresponding power of 2, i.e. 64, 32, 16, 8, 4, 2, 1. In the next adjacent cell AB1, use the sum formula `=SUM(S1:Z1)`.

Now copy the formulae in the first row to all the rows. The best way to do this is to highlight the cells with formulas in row 1 using `Ctrl + Shift + End` and then apply the formulae with `Ctrl + D`. Once Excel has finished applying the formulae, copy the entire AB column by clicking on it. Convert it to ASCII using an online tool such as [RapidTables](https://www.rapidtables.com/convert/number/ascii-hex-bin-dec-converter.html). The flag is somewhere in the text.

The flag is `MACS{c0pY_p45t4}`

