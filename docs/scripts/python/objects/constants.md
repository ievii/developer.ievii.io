# Constants

In the script there may be some constants we need to know

## ColumnTypes

!!! question "ColumnTypes"

    Column type, when insert/add columns, change column types, etc. need to be used

    ```python
    from seatable_api.constants import ColumnTypes

    ColumnTypes.NUMBER              # number
    ColumnTypes.TEXT                # text
    ColumnTypes.LONG_TEXT           # long text
    ColumnTypes.CHECKBOX            # checkbox
    ColumnTypes.DATE                # date & time
    ColumnTypes.SINGLE_SELECT       # single select
    ColumnTypes.MULTIPLE_SELECT     # multiple select
    ColumnTypes.IMAGE               # image
    ColumnTypes.FILE                # file
    ColumnTypes.COLLABORATOR        # collaborator
    ColumnTypes.LINK                # link to other records
    ColumnTypes.FORMULA             # formula
    ColumnTypes.CREATOR             # creator
    ColumnTypes.CTIME               # create time
    ColumnTypes.LAST_MODIFIER       # last modifier
    ColumnTypes.MTIME               # modify time
    ColumnTypes.GEOLOCATION         # geolocation
    ColumnTypes.AUTO_NUMBER         # auto munber
    ColumnTypes.URL                 # URL
    ```
