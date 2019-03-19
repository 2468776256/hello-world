# hello-world
# 奇数幻方
# test1
def output(test,n):      #打印幻方
    i=0
    while i<n :
        print(test[i])
        i=i+1
def magic_supare(square,n):    #创建幻方函数
        square[0][int((n-1)/2)]=1
        i=0
        j=int((n-1)/2)
        value=1
        while value<n*n :
            i=i-1
            j=j+1
            value=value+1
            if j==n:
                j=0
            if i==-1:
                i=n-1
            if i!=n-1 and j==0 and square[i][j]!=0:
                j=n-1
                i=i+2
            elif i==n-1 and j==0 and square[i][j]!=0:
                j=n-1
                i=1
            elif square[i][j]!=0:
                i=i+2
                j=j-1
            square[i][j]=value
        return 1

print("please input the order of the magic square ")
t=input()
n=int(t)
test =[[0 for i in range(n)] for i in range(n)]
magic_supare(test,n)   
output(test,n) 


