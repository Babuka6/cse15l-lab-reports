# CSE15L -- Anthony Chapov -- Lab 3 -- 1. Testing and Debugging 2. Researching command's variations. 


## A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown):

### First input: 
Note that we inputp1 containts multiple copies of lowest value. We want to lowest value from the list, but what if there are few copies of same lowest value?
```

@Test
  public void testAvg4() {
    double[] input1 = {0.4,4.1,2.9,3.5,0.4}; //bug 
    assertEquals(3.5, ArrayExamples.averageWithoutLowest(input1),0.05);

  }
```

### Second input:
Note that here we have just 1 single element that is not copy of minimum value. So the average must consider just 4 because 2 and any of its copies must be excluded. Right?

```

@Test
  public void testAvg7() {
    double[] input1 = {2,2,2,2,2,4,2}; //including multiple copies of min el.
    assertEquals(4, ArrayExamples.averageWithoutLowest(input1),0.05);

}  
```

## An input that doesn’t induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown)
 
### First input:
Note: runs good because no duplicates. 

```
@Test
  public void testAvg5() {
    double[] input1 = {1,4.5,-2,3.4,0}; //including zero and negative value
    assertEquals(2.225, ArrayExamples.averageWithoutLowest(input1),0.05);
    
  }
```

### Second input:
Note: runs good because 2 is minimum value. Thus, any of its copies excluded from calculation. Excluding all 2's leaves us with {} list. In this case sum is not incremented and is still 0. Diving 0 by array's size (other than 0 of course) works correctly and produces 0. It is because for the calculation excluding minimum, we exclude all elements and thus take average of "nothing": zero as answer make sense. 

```
@Test
  public void testAvg6() {
    double[] input1 = {2,2,2}; 
    assertEquals(0, ArrayExamples.averageWithoutLowest(input1),0.05);
   //excluding minimum in this case is excluding all copies of 
   //minimum ->size < 2 -> 0 
  }
```
## The symptom, as the output of running the tests (provide it as a screenshot of running JUnit with at least the two inputs above)
![symptom](symptom.JPG)

## The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown)

### Original code: 

```
static double averageWithoutLowest(double[] arr) {
  if(arr.length < 2) { return 0.0; }
  double lowest = arr[0];
  for(double num: arr) {
  if(num < lowest) { lowest = num; }
  }
  double sum = 0;
  for(double num: arr) {
  if(num != lowest) { sum += num; }
  }
  return sum / (arr.length - 1);
  } 
```

### Beatiful, magnificient, superb code (fixed):

```
static double averageWithoutLowest(double[] arr) {
    if(arr.length < 2) { return 0.0; }
    double lowest = arr[0];
    for(double num: arr) {
      if(num < lowest) { lowest = num; }
    }
    double sum = 0;
    int duplicatesOfMin = 0;

    for(double num: arr) {
      if(num != lowest) { sum += num; }
      else if (num == lowest) {duplicatesOfMin++; }
    }
    if (arr.length != duplicatesOfMin)
    return sum / (arr.length - duplicatesOfMin);
    else
    {
      return 0;
    }
  }

Time: 0.012

OK (13 tests)
```

## Briefly describe why the fix addresses the issue:
As we can see in the failure-producing input, whenever we have more than 1 copies of minimim value that we want to exclude, the original code excludes only one 




