# Minimum Number of Platforms

~~~
int calculateMinPatforms(int at[], int dt[], int n) {
  sort(at, at + n);
  sort(dt, dt + n);

  int Pltcount = 1, i = 1, j = 0;

  while (i < n) {
    if (at[i] > dt[j])
      j++;
    else
      Pltcount++;
    i++;
  }
  return Pltcount;
}
~~~
