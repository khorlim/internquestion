import json

output = []
for i in range(1,101):
    if i % 3==0 and i % 5 == 0:
        output.append("BIGBANG")
    elif i % 3 == 0:
        output.append("BIG")
    elif i % 5 == 0:
        output.append("BANG")
    else:
        output.append(str(i))

file = open('output.json', 'w')
json.dump(output, file)