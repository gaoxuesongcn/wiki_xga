cut
============

> -b for bytes  
> -c for characters  
> -f for defining fields  

>N- from the Nth byte, character, or field, to the end of the line  
>N-M from the Nth to Mth (included) byte, character, or field  
>-M from the first to Mth (included) byte, character, or field

```shell
cut -f 1,2 -d "," supplied_source.csv
```
```shell
cut -c 1-5,6-9 supplied_source.csv
```



```shell
cut --complement -f 1,2 -d "," supplied_source.csv
```
