# Lab Report3
Bugs and Commands

# Part 1 - Bugs
Provide:
- A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown)
- An input that doesn’t induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown)
- The symptom, as the output of running the tests (provide it as a screenshot of running JUnit with at least the two inputs above)
- The bug, as the before-and-after code change required to fix it (as two code blocks in Markdown)
Briefly describe why the fix addresses the issue.

1. A failure-inducing input for the buggy program, as a JUnit test and any associated code (write it as a code block in Markdown)
JUnit Test:
```
@Test
  public void testReverseInPlace2() {
    int[] input1 = { 3,2,1,0 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 0,1,2,3 }, input1);
	}
```
Associated code:
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
2. An input that doesn’t induce a failure, as a JUnit test and any associated code (write it as a code block in Markdown)
JUnit Test:
```
@Test 
	public void testReverseInPlace() {
    int[] input1 = { 0,1,0 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 0,1,0 }, input1);
	}

```
Associated code:
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
3. Screenshot for the Symptom
![Image](CSE15L_LabReport3_ScreenShotForSymptom.png)

4. The Bug, as the before-and-after code change required to fix it (as two code blocks in Markdown)
Before Code:
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
After Code:
```
  static void reverseInPlace(int[] arr) {
    int[] temp = arr.clone();
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = temp[arr.length - i - 1];
    }
  }
```
The fix was creating a temp array that stores the original array and change each part of the array reversed from the temporary stored array.