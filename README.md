# Anagrams-problem-by-hackerearth
n=int(input())
for i in range(n):
    c=0
    d={};e={}
    j=input()
    k=input()
    for m in j:
        if m in d:
            d[m]+=1
        else:
            d[m]=1
    for m in k:
        if m in e:
            e[m]+=1
        else:
            e[m]=1
    for i in d:
        if i in e:
            c+=abs(d[i]-e[i])
        else:
            c+=d[i]
    for i in e:
        if i not in d:
            c+=e[i]
    print(c)
