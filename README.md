# Tri-Fusion
(7,24,19,17,10,6,1)

def triFusion(list):
    if len(list)<=1:
        return list

    else:
        mid=len(list)//2
        L1=list[0:mid]
        L2=list[mid:]
        L1T=triFusion(L1)
        L2T=triFusion(L2)

        return fusion(L1T,L2T)

def fusion(list1, list2):
    listR=[]
    for i in list1:
        j=0
        while j<len(list2) and list2[j]<i:
            j=j+1
        listR.append(i)
        listR.extend(list2[j:])

print(triFusion([7,24,19,17,10,6,1]))



Cynthia Samouelian
GD1.2

        

    

    
