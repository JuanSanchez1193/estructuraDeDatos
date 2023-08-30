numero_casos = int(input())
lista_casos = []  # [[333], [111, 111]]
for i in range(numero_casos):
    caso_converted_to_integer = []
    caso = input().split(" ")
    for i in caso:
        caso_converted_to_integer.append(int(i))
    lista_casos.append(caso_converted_to_integer)
def contador(list):
    list_counters = []
    for caso in list:
        caso = sorted(caso)
        counter = {}
        for numero in caso:
            if numero not in counter:
                counter[numero] = 1
            else:
                counter[numero] += 1
        list_counters.append(counter)
    return list_counters
diccionary = contador(lista_casos)
for i in diccionary:
    list =(i.items())
    for tupla in list:
        print(tupla[1])


lenght = int(input())
string_list = input().split(" ")
number_cases = int(input())
cases_list_string = input().split(" ")
def convert_to_int(list):
    return [int(string) for string in list]
int_list = convert_to_int(string_list)
cases_list_int = convert_to_int(cases_list_string)
def master(list1,list2):
    counter = 0
    for i in list2:
        if i in list1:
            counter += list1.index(i) +1
    return counter
print(master(int_list,cases_list_int))
