import java.util.Scanner;
import java.util.ArrayList;
import java.util.HashSet;

public class Solution {
public static void main(String[] args) {

  Scanner sc = new Scanner(System.in);
  int n = sc.nextInt();
  ArrayList<Integer> list = new ArrayList<Integer>();
  
  while(n > 0){
    list.add(n % 10);
    n = n / 10;
  }
  
HashSet<Integer> distinct = new HashSet<>();
HashSet<Integer> repetitive = new HashSet<>();
for (int i: list) {
    if (distinct.contains(i)) {
        repetitive.add(i);
    } else {
        distinct.add(i);
    }
  
  }
  if(repetitive.size() > 0){
    System.out.println("Yes");
  }
  else{
    System.out.println("No");
  }
 
}
}
