1)
foot_dict= {
   'Россия' 'A',
   'Португалия' 'B',
   'Франция' 'C',
   'Дания' 'C',
   'Египет' 'A'
}

foot_dict['Турция']='B'
print(foot_dict)

group=input()

for i in foot_dict:
   if foot_dict[i]==group:
       print(i)

unig=list(set(foot_dict.values()))
ug=dict.fromkeys(unig,0)


for i in foot_dict:
   ug[foot_dict[i]]+=1

print(ug)
 
2)
pointsForLetters = {
   1:['A', 'E', 'I', 'L', 'N', 'O', 'R', 'S', 'T', 'U'],
   2:['D', 'G'],
   3:['B', 'C', 'M', 'P'],
   4:['F', 'H', 'V', 'W', 'Y'],
   5:['K'],
   8:['J', 'X'],
   10:['Q', 'Z']}

word = input('Введите слово(англ) ').upper()
score = 0
for i in word:
   for j in pointsForLetters.keys():
       if j in pointsForLetters[j]:
           score += j

print(score)
 
3)
with open('run_of_60_m.txt', 'r') as f:
   data = f.read()
data = data.split('\n')
item = None
for i in data:
   item = i.split(" ")
   print(item)
   gender = item[0]
   grade = int(item[1])
   surname = item[2]
   time = float(item[3])
   if gender == 'Д':
       if grade ==7:
           if time <= 9.8:
               print(surname, 5)
           elif time <= 10.6:
               print(surname, 4)
           elif time <= 11.4:
               print(surname, 3)
           else:
               print(surname, 2)
       elif grade ==6:
           if time <= 10.3:
               print(surname, 5)
           elif time <= 10.6:
               print(surname, 4)
           elif time <= 11.2:
               print(surname, 3)
           else:
               print(surname, 2)
   if gender == 'М':
       if grade ==7:
           if time <= 9.4:
               print(surname, 5)
           elif time <= 10.2:
               print(surname, 4)
           elif time <= 11.0:
               print(surname, 3)
           else:
               print(surname, 2)
       elif grade ==6:
           if time <= 9.9:
               print(surname, 5)
           elif time <= 10.4:
               print(surname, 4)
           elif time <= 11.1:
               print(surname, 3)
           else:
               print(surname, 2)
