#                                                         FUNCTIONS-2-UNIT3
    CAROLINA TORRES ARJONA.
    DATA 1A.
# MAX 3 NUMBERS
# EX01.PY

    def MAX2(x,y):
      if x > y:
        return x
      else:
        return y

    def MAX3(x,y,z):
      return MAX2(x, MAX2(y,z))

    print(MAX3(10,2,6))

# EX01.C

    #include <stdio.h>
    //MAX OF 3 NUMBERS USING FUNCTIONS
    int N1,N2,N3,max2,max3;

    int MAX2(x,y)
    {
      if(x>y)
      max2=x;
      else
      max2=y;
      return max2;
    }

    int MAX3(x,y,z)
    {
    max3=MAX2(x,MAX2(y,z));
    return max3;
    }

    int main() {
      printf("INTRODUCE TUS 3 NUMEROS\n");
      scanf("%i %i %i", &N1, &N2, &N3);
      printf("\n%i",MAX3(N1,N2,N3));
      return 0;
    }
    
# SUM NUMBERS
# EX02.PY

    #Write a Python function to sum all the numbers in a list. 
    #Sample List : (8, 2, 3, 0, 7)
    #Expected Output : 20

    def SUMA(numbers):
      sum=0
      for x in numbers:
        sum+=x
      return sum

    print(SUMA((8, 2, 3, 0, 7)))

# EX02.C

    #include <stdio.h>

    int SUMA(int x)
    {
      int SUM;
      SUM=0;
      SUM=SUM+x;
      return SUM;
    }

    int main() {
      printf("%i", SUMA(7));
      return 0;
    }

# MULTIPLY NUMBERS
# EX03.PY

    #Write a Python function to multiply all the numbers in a list. Go to the editor
    #Sample List : (8, 2, 3, -1, 7)
    #Expected Output : -336 

    def mult(numbers):
      multi=1
      for x in numbers:
        multi*=x
      return multi

    print(mult((8, 2, 3, -1, 7)))


# EX03.C

    #include <stdio.h>

    int MULT(int x)
    {
      int M;
      M=1;
      M=M*x;
      return M;
    }

    int main() {
      printf("%i", MULT(7));
      return 0;

    }

# INVERT STRING
# EX04.PY

    #3Write a Python program to reverse a string. Go to the editor
    #Sample String : "1234abcd"
    #Expected Output : "dcba4321"

    def inve(string):
        w=''
        i=0
        x=len(string)
        for i in string:
            w += string[ x - 1 ]
            x = x-1
        return w
    print(inve('olmar'))

    def string_reverse(str1):

        rstr1 = ''
        index = len(str1)
        while index > 0:
            rstr1 += str1[ index - 1 ]
            index = index - 1
        return rstr1
    print(string_reverse('1234abcd'))

# EX04.C

    #include <stdio.h>
    #include <string.h>

    /*create a function that receives a string 
    and print the inverted string]*/
    char S[30];

    void INVERT(char x[])
    {
      char inv[30];
      int i, ll,c;
      c=0;

      ll=strlen(x);
      for(i=ll-1;i>=0;i--)
      {
        inv[c]=x[i];
        c=c+1;
      }
      printf("%s",inv);
    }

    int main() {

      fgets(S,30,stdin);
      INVERT(S);

      return 0;
    }

# FACTORIAL
# EX05.PY

    # Write a Python function to calculate the 
    # factorial of a number (a non-negative integer).
    # The function accepts the number as an 
    # argument.

    def fac(n):
        if n == 0:
            return 1
        else:
            return n * fac(n-1)
    n=int(input("Input a number to compute the factiorial : "))
    print(fac(n))

# EX05.C
 
    #include <stdio.h>

    int fac(int x)
    {
      int i, f;
      f=1;
      for(i=1;i<=x;i++)
        f=f*i;

    return f;
    }

    int main() {
      int N;
      printf("INTRODUCE N\n");
      scanf("%i",&N);
      printf("\n%i",fac(N));
      return 0;
    }
    
# NUMBER WITHIN OR OUT OF A RANGE
# EX06.PY

    #Write a Python function to check whether
    #a number is in a given range


    def wrange(n):
        if n>=l and n<=h:
            return print("WITHIN THE RANGE")
        else:
            return print("OUT OF THE RANGE")

    l=int(input("low limit  : "))
    h=int(input("high limit : "))
    n=int(input("Number to know if is within the range: "))
    print(wrange(n))

# EX06.C

    #include <stdio.h>
    //PROGRAMM TO KNOW IF A NUMBER IS WITHIN A RANGE
    int l,h,n;

    void range(int x, int y, int z)
    {
      int i;
    if(z>=x&&z<=y)
    printf("IS WITHIN THE RANGE");
    else
    printf("IS OUT OF THE RANGE");
    } 

    int main() {

      printf("INTRODUCE LOW LIMIT\n");
      scanf("%i",&l);
      printf("INTRODUCE HIGH LIMIT\n");
      scanf("%i",&h);
      printf("INTRODUCE NUMBER\n");
      scanf("%i",&n);
      range(l,h,n);
      return 0;
    }

# UPPER AND LOW CASE LETTERS
# EX07.PY

    #Write a Python function that accepts a string
    #and calculate the number of upper case letters
    #and lower case letters. Go to the editor
    #Sample String : 'The quick Brow Fox'
    #Expected Output : 
    #No. of Upper case characters : 3
    #No. of Lower case Characters : 12

    def upoelow(s):
        v={"UPPER":0, "LOWER":0}
        for c in s:
            if c.isupper():
               v["UPPER"]+=1
            elif c.islower():
               v["LOWER"]+=1
            else:
               pass#!!!!!!

        print ("No. of Upper case characters : ", v["UPPER"])
        print ("No. of Lower case Characters : ", v["LOWER"])

    s=(input("INTRODUCE WORD : "))
    upoelow(s)

# EX07.C

    #include <stdio.h>
    #include <string.h>
    #define MAX 30

    char S1[MAX];

    void upalo(char x[MAX])
    {
      int i, u, l;
      u=0;
      l=0;
    for(i=0;i<=strlen(x);i++)
    {
      if(x[i]>='A'||x[i]<='Z')
      u=u+1;
      else if(x[i]>='a'||x[i]<='z')
      l=l+1;
    }
    printf("\nNO. UPPER CASE: %i",u);
    printf("\nNO. LOWER CASE: %i",l);


    }

    int main()
    {
      printf("INTRODUCE THE WORD\n");
      fgets(S1,MAX,stdin);
      upalo(S1);
      return 0;
    }

# UNIQUE ELEMENTS
# EX08.PY

    #Write a Python function that takes a list
    #and returns a new list with unique elements 
    #of the first list. 
    #Sample List : [1,2,3,3,3,3,4,5]
    #Unique List : [1, 2, 3, 4, 5]

    def uniq(number):
      x = []
      for a in number:
        if a not in x:
          x.append(a)
      return x

    print(uniq([1,2,3,3,3,3,4,5])) 

# EX08.C

    #include <stdio.h>
    int main()
    {
        int arr1[30], n, ctr;
        ctr=0;
        int i, j, k;

       printf("HOW MANY: ");
       scanf("%i",&n);
      
       for(i=0;i<n;i++)
            {
	      printf("element");
	      scanf("%d",&arr1[i]);
	    }
    printf("\nUNIQUE ELEMENTS: \n");
    for(i=0; i<n; i++)
    {
        ctr=0;
        for(j=0,k=n; j<k+1; j++)
        {
            if (i!=j)
            {
		       if(arr1[i]==arr1[j])
              {
                 ctr=ctr+1;
               }
             }
        }
       if(ctr==0)
        {
          printf("%d ",arr1[i]);
        }
    }
       printf("\n\n");
}

# PRIME OR NOT
# EX09.PY

    #Write a Python function that takes
    #a number as a parameter and check the 
    #number is prime or not.
    #Note : A prime number (or a prime) is a 
    #natural number greater than 1 and that has 
    #no positive divisors other than 1 and itself. 
    #FIRST TIME USING RANGE!!!!!
    def prime(n):

    if (n==1):
        return print("IT IS")
    elif (n==2):
        return print("IT IS")
    else:
        for x in range(2,n):
            if(n % x==0):
                return print("IT IS NOT")
        return print("IT IS")       

    print(prime(2))

# EX09.C

    #include <stdio.h>
    int num1;

    void prime(int x)
    {
    int i,a;
    a=0; 

      for(i=1;i<=x;i++)
      {
          if(x%i==0) 
          a++;
      }

      if(a==2) 
      {
          printf("El número es primo");
      }
      else
      {
          printf("El número no es primo"); 
      }

    }

    int main()
    {
    printf("Introduce un numero: ");
    scanf("%d",&num1);
    prime(num1);
    }

# EVEN NUMBERS FROM A RANGE
# EX10.PY

    #Write a Python program to print the even
    #numbers from a given list. Go to the editor
    #Sample List : [1, 2, 3, 4, 5, 6, 7, 8, 9] 
    #Expected Result : [2, 4, 6, 8]
    #append!!!!

    def even(numbers):
        x = []
        for i in numbers:
            if i % 2 == 0:
                x.append(i)
        return x
    print(even([1,4,5,4,6,7,10 ]))

# EX10.C

    #include <stdio.h>
    //FUNCTION TO EVEN NUMBERS
    void even(x,y)
    {
      int i;
    for (i =x ; i <= y; i++) 
    {
        if (i % 2 == 0) 
          printf("%d ", i);
    }
    }

    int main() {
      int l, h;
      printf("low range:\n");
      scanf("%d", &l);
      printf("high range:\n");
      scanf("%d", &h);
      even(l, h);

      return 0;
    }
    
# PERFECT NUMBER
# EX11.PY 

    #PERFECT NUMBER

    def perf(n):
        sum = 0
        for x in range(1, n):#TO STOP IN THE NUMBER AND START IN 1
            if n % x == 0:
                sum += x
        return sum == n
    print(perf(12))

# EX11.C

    #include <stdio.h>
    //PERFECT NUMBER
    int N1;

    int CARITO(int x)
    {
      int i, sum;
      sum=0;
      for(i=1;i<x;i++)
      {
        if((x%i)==0)
        {
          printf("\n%i", i);
          sum=sum+i;
          printf("\n%i", sum);
        }
      }
      return sum;
    }

    void CARITO2(int x)
    {
      int c;
      c=CARITO(x);
      if(c==x)
      {
        printf("IS PERFECT");
      }
      else
        printf("IS NOT PERFECT");
    }

    int main(void) {

      printf("ENTER THE NUMBER\n");
      scanf("%i",&N1);
      CARITO2(N1);
      return 0;
    }
    
# PALINDROMIC
# EX12.PY

    #PALINDROMO 
    def PALI(string):
      menor = 0
      mayor = len(string) - 1

      while mayor >= menor:
        if not string[menor] == string[mayor]:
          return False
        menor += 1
        mayor -= 1
      return True
    print(PALI('ararara')) 

# EX12.C

    #include <stdio.h>
    #include <string.h>
    #define MAX 30
    // PALINDROMO 
    char S[MAX];

    int INVERT(char x[MAX])
    {
      int mylen, i, ol;
      ol=0;
      mylen = strlen(x)-1;
    for(i=mylen-1;i>=0;i--)//VA REVIRTIENDO LA PALABRA
      {

        if(x[i]!=x[mylen-i-1])//COMPARA LOS CARACTERES
        {
        ol=ol+1;
         break;//CON UNO QUE ENCUENTRE DIFERENTE DEJA DE COMPARAR
        }
        else 
        {
        ol=ol+0;//LA SUMA DA 0 CUANDO NO HAY NINGUNA DIFERENCIA
        }
      }
      return ol;
    }

    int main() 
    {
      int resultado;
      fgets(S,MAX,stdin);
      resultado=INVERT(S);//LLAMO LA FUNCION METIENDOLA EN UNA VARIABLE DE ETSA FUNCION
      if(resultado!=0)
      {
        printf("0 NO ES PALINDROMO");
      }
      else
        printf("1 SI ES PALINDROMO");
    return 0;
    }
