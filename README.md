# highpeakcodingtest
dictionary= {}
with open("input.txt") as f:
  for line in f:
    (key, val) = line.split(':')
    dictionary[key] = int(val.strip())

dictvalues_list=list(dictionary.values())
dictkeys_list=list(dictionary.keys())
dict_list=list(dictionary.values())



number=int(input("Enter the number of employees\n"))
k=len(d_list)-number
d_list.sort()
l=0
r=len(d_list) -1
for i in range(k):
  if(d_list[r-1] - d_list[l] < d_list[r] - d_list[l+1]):
      r-=1
  else:
      l+=1
diff=d_list[r]-d_list[l]
with open("output.txt",'w') as fi:
  fi.write("Here the goodies that are selected for distribution are:\n")
  for i in range(l,r+1):
    position = du_list.index(d_list[i])
    fi.write(k_list[position]+": "+ str(d[k_list[position]])+"\n")
  fi.write("\nAnd the difference between the chosen goodie with highest price and the lowest price is "+str(diff))
