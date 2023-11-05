CSE15L -- Anthony Chapov -- Lab 3 -- 1. Testing and Debugging 2. Researching command's variations. 


A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown):

First input: 
```
{
@Test
  public void testAvg4() {
    double[] input1 = {0.4,4.1,2.9,3.5,0.4}; //bug 
    assertEquals(3.5, ArrayExamples.averageWithoutLowest(input1),0.05);

  }
```

Second input:
```
{
@Test
  public void testAvg7() {
    double[] input1 = {2,2,2,2,2,4,2}; //including multiple copies of min el.
    assertEquals(4, ArrayExamples.averageWithoutLowest(input1),0.05);
    
  }
```
