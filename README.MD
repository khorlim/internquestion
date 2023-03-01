import json

# Create a empty list 
output = []

# Iterate from 1 to 100 
for i in range(1,101):

    # if the number can be divided by 3 and 5 append BIGBANG
    if i % 3==0 and i % 5 == 0:
        output.append("BIGBANG")
    
    # if the number can only be divided by 3 append "BIG"
    elif i % 3 == 0:
        output.append("BIG")
    
    # if the number can only be divided by 5 append "BANG"
    elif i % 5 == 0:
        output.append("BANG")
    
    # Else append the number
    else:
        output.append(str(i))
    
# Create file if not exist or open the file 
file = open('output.json', 'w') 

#Write file 
json.dump(output, file)
