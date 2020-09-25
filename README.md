# num-to-words
To print the numbers into words upto a certain range
#To print the numbers in letters upto a certain range
def num_to_words(x):
    if x==0:
        return 
    a=['zero','one','two','three','four','five','six','seven','eight','nine']
    return a[x]
def num_to_words2(x):
    b=['ten','twenty','thirty','fourty','fifty','sixty','seventy','eighty','ninty']
    return b[x-1]
def num_to_words3(z):
    c={11:'eleven',12:'twelve',13:'thirteen',14:'fourteen',15:'fifteen',16:'sixteen',17:'seventeen',18:'eighteen',19:'ninteen'}
    return c[z]
r=int(input('Enter the range between 0-1000:'))
for o in range(0,r+1):
    if o==0:
            print('zero',end=' ')
            continue
    elif o>10 and o<20:
        print()
        print(num_to_words3(o),end=' ')
        continue
    o=str(o)
    print()
    if int(o)%100==0:
        print(num_to_words(int(o[0])),end=' ')
        if len(o)==3:
            print('hundred',end=' ')
        elif len(o)==4:
            print('thousand',end=' ')
    else:
        s=len(o)
        k=[]
        for i in o:
            k.append(int(i))
        for i in k:
            if i!=0:
                if s==2:
                    print(num_to_words2(i),end=' ')
                    s-=1
                    continue
            if i!=0:
                print(num_to_words(i),end=' ')
            if s==3:
                print('hundred and',end=' ')
            s-=1
