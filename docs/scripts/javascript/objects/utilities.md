# Utility functions

Utility functions help you to work with data in SeaTable.

## Date and Time

!!! success "formatDate"

    Format date to 'YYYY-MM-DD' to be used in a date column.

    ``` js
    base.utils.formatDate(date: date object)
    ```

    __Example__
    ``` js
    let date = new Date();
    let formatDate = base.utils.formatDate(date);
    output.text(formatDate);
    ```

!!! success "formatDateWithMinutes"

    Format date to 'YYYY-MM-DD HH:mm' to be used in a date column..

    ``` js
    base.utils.formatDateWithMinutes(date: date object)
    ```

    __Example__
    ``` js
    let date = new Date();
    let formatDate = base.utils.formatDateWithMinutes(date);
    output.text(formatDate);
    ```

## Lookup and Query

!!! success "lookupAndCopy"

    Similar to the vlookup function in Excel. Find a matching row in the source table for each row of the target table, and then copy the data of the specified cell of the matching row to the specified cell of the target row.

    | Name | Email |
    | ---  | --- |
    | Hulk | greenbigboy@stark-industries.movie |
    | Tony | ironman|stark-industries.movie |

    The target table only has the user names but we want to copy the email address from the source table to the target table, then this function can be used.

    | Name | Email |
    | ---  | --- |
    | Hulk | |
    | Tony | |

    ``` js
    base.utils.lookupAndCopy(targetTable, targetColumn, targetColumnToCompare, sourceTableName, sourceColumnName, sourceColumnToCompare = null);
    ```

    __Example__

    ``` js
    // Match the rows with the same content in the Name column of Table1 and Table2, copy the contents of the Email column of the row in Table1 to the Email column of the corresponding row in Table2
    base.utils.lookupAndCopy('Table2', 'Email', 'Name', 'Table1', 'Name');

    // Match the rows with the same content in the Name column in Table1 and the Name1 column in Table2, and copy the contents of the Email column of the row in Table1 to the Email1 column of the corresponding row in Table2
    base.utils.lookupAndCopy('Table2', 'Email1', 'Name1', 'Table1', 'Email', 'Name');

    ```

!!! success "query"

    Filter and summary the table data by SQL like statements.

    ``` js
    base.utils.query(tableName: String, viewName: String, query: String);
    ```

    __Example__

    ``` js
    // Filter out the rows where the sum of the three columns 'number', 'number1', and 'number2' is greater than 5 then sum the number and number2 columns in these rows, return {number: 12, number2: 23}
    base.utils.query('Table1', 'View_name', 'select sum(number), sum(number2) where number + number1 + number2 > 5');
    ```
