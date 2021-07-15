# pythonassinment2
dic = {'a': 'Hello', 'b': 'World', 'c': 'Buddy'}

i = input().split()
if len(i) == 3 and (i.count('and') == 1 or i.count('or') == 1):
    a, operator, b = i
elif len(i) == 5 and (i.count('and') == 2):
    a, operator_one, b, operator_two, c = i 

if len(i) == 3:
    if operator == 'and':
        print(f'{dic[a]}{dic[b]}')
    elif (operator == 'or'):
        try: 
            print(f'{dic[a] or {dic[b]}}')
        except KeyError:
            print(f'{dic[b] or dic[a]}')
if len(i) == 5:
    if operator_one == 'and' and operator_two == 'and':
        print(f'{dic[a]}{dic[b]}{dic[c]}')
