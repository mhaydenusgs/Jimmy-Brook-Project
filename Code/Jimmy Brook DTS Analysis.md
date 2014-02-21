### Load Data

```r
DTS <- read.csv("DTS Data.csv", header = T)
```

```
## Warning: cannot open file 'DTS Data.csv': No such file or directory
```

```
## Error: cannot open the connection
```


### Modify the Data

```r
x <- DTS[1:3960, ]
```

```
## Error: object 'DTS' not found
```

```r
y <- DTS[3961:7920, ]
```

```
## Error: object 'DTS' not found
```

```r
head(x)
```

```
## Error: object 'x' not found
```


### Plot the DTS Data in Whole then split up form

```r
### Basic Plot in Plot to see what is there
plot(DTS$Cable.Length, DTS$Temperature)
```

```
## Error: object 'DTS' not found
```

```r

### Formal Plot in GGplot
ggplot(DTS, aes(x = Cable.Length, y = Temperature)) + geom_line(aes(fill = "Temperature"))
```

```
## Error: could not find function "ggplot"
```

```r

### Half of the cable length
ggplot(x, aes(x = Cable.Length, y = Temperature)) + geom_line(aes(fill = "Temperature"))
```

```
## Error: could not find function "ggplot"
```


### Plot the Difference between one side of the Cable to the Other

```r
x1 <- x$Temperature
```

```
## Error: object 'x' not found
```

```r
y1 <- y$Temperature
```

```
## Error: object 'y' not found
```

```r
z <- x1 - y1
```

```
## Error: object 'x1' not found
```

```r
g <- 1:3960
Z <- data.frame(g, z)
```

```
## Error: object 'z' not found
```

```r
ggplot(Z, aes(x = g, y = z)) + geom_line(aes(fill = "z"))
```

```
## Error: could not find function "ggplot"
```

