Dao层直接wrap返回给上层

```go
func Datas() error {
	_, err := db.Exec(" sql ")
	if err != nil { 
        return errors.Wrap(err,"ErrNoRows") 
	}
	return nil
}
```