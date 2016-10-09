# Excel Formula Utilities for JavaScript



## ExcelFormulaBeautifier.com
To submit pull requests for ExcelFormulaBeautifier.com please oppen a pull request after gh-pages branch.
To submit pull requests for [ExcelFormulaBeautifier.com](http://ExcelFormulaBeautifier.com) please use this branch.
Changes to the core js library live in the master branch.

##Install using npm
npm install excel-formula

## Installation for web
Grab the latest js files in the dist folder.

## Basic usage for web
    <script src="excel-formula.js" />
    <script>
        var formattedFormula = excelFormulaUtilities.formatFormulaHTML('IF(1+1=2,"true","false")');
        alert(formattedFormula)
    </script>

## Basic Usage for Node
    var formula = require('excel-formula'); // original package name
    var formattedFormula = formula.formatFormula('IF(1+1=2,"true","false")');
    console.log(formatFormula);

## Node methods
See basic usage above.
```javascript
    formula.getTokens (formula);
    formula.formatFormula (formula, [opts])
    formula.toJavaScript(formula)
    formula.toCSharp(formula)
```
## Web methods
excelFormulaUtilities is a global variable.
```javascript
    excelFormulaUtilities.getTokens (formula);
    excelFormulaUtilities.formatFormula (formula, [opts]) // This will work fine in a pre tag
    excelFormulaUtilities.formatFormulaHTML(formula) // Use this if you want the output as html.
    excelFormulaUtilities.formula2JavaScript(formula)
    excelFormulaUtilities.formula2CSharp(formula)
```
