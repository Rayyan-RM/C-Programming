# C-Programming

# Task
#There is a series, S, where the next term is the sum of pervious three terms. Given the first three terms of the series, a, b, and c respectively, you have to output the nth term of the series using recursion.
#Input Format
• The first line contains a single integer, n.
• The next line contains 3 space-separated integers, a, b, and c


#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>
//Complete the following function.

int find_nth_term(int n, int a, int b, int c) {
    
    if(n==1){
        return a;
    }
    else if (n==2){
        return b;
    }
    else if (n==3){
        return c;
    }
    else {
        return find_nth_term(n-1,a,b,c)+find_nth_term(n-2,a,b,c)+find_nth_term(n-3,a,b,c);
        }
        
    
}

int main() {
    int n, a, b, c;
  
    scanf("%d %d %d %d", &n, &a, &b, &c);
    int ans = find_nth_term(n, a, b, c);
 
    printf("%d", ans); 
    return 0;
}

