# Composr perf tests

## Init

`pm2=true corbel-composr`

## Attack

This project uses [vegeta](https://github.com/tsenart/vegeta) to create graphs with the results

```
vegeta attack -duration=3600s -rate=10 -targets=targets.txt > results.bin
```

## Generate reports

```
cat results.bin | vegeta report -reporter=plot > plot.html
```


## Generate more endpoints

Run `composr -g` to add new endpoints to the project. Edit or create new targets and test cases :)