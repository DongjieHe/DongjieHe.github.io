# sun.nio.cs.StandardCharsets$Aliases:init
```Java
protected void init(Object[] param) {
  x = newArray Object[2];
  x[0] = "cs...";
  x[1] = "cie...";
  param[1] = x;
  ...
  x1015 = newArray Object[2];
  x1015[0] = "xxx";
  x1015[1] = "xxxx";
  param[1015] = x1015;
}
super:<init> {
  this.ht = new Object[...];
  init(this.ht);
}
```
