def Q(question):
    postQuestion(question)

def printAnimalNames(myAnimals):
    animalNames = ''
    for x in myAnimals:
        #print('current animal == ' +str(x))
        if len(animalNames) > 0:
           animalNames = animalNames + ', ' + x.get('name')
        else:
            animalNames = x.get('name')
       
    print ('names of my animals: ' +animalNames)

def printAnimalStats(myAnimals, species):
    pluralSpecies = species + 's'
    stats = calculateStats(myAnimals, species, pluralSpecies)
    if stats != None:
        print('my '+pluralSpecies + ' weight '+ str(stats.get('averageWeight')) + ' kg\'s on average and are '
              + str(stats.get('averageAge')) +' years old. Together my ' + pluralSpecies + ' are ' +str(stats.get('totalAge')) + ' years old.')
    else:
        print('I don\'t have '+pluralSpecies)

def calculateStats(animals, species, pluralSpecies):
    totalWeight = 0
    totalAge = 0
    countOfSpecies = 0
    averageWeight = None
    averageAge = None
    stats = None
    print('my ' + pluralSpecies +' stats -------->')
    for x in animals:
        if x.get('type') == species:
            totalWeight += x.get('weight')
            totalAge += x.get('age')            
            countOfSpecies  +=1
            print (x.get('name') + ' weights ' +str(x.get('weight'))+ ' kg and age '+str(x.get('age')))
    if countOfSpecies > 0:
        averageWeight = round(totalWeight / countOfSpecies, 1)
        averageAge = round(totalAge / countOfSpecies, 1)
        stats = {'averageWeight' : averageWeight, 'averageAge' : averageAge , 'totalAge' : totalAge}
    return stats

def postQuestion(question):
    # animal attributes
    crododile = {'species' : 'crocodile', 'character' : 'angry'}
    dog = {'species' : 'dog', 'character' : 'furry'}
    cat = {'species' : 'cat', 'character' : 'funny'}
    santtu = {'species' : 'santtu', 'character' : 'cool'}
    animalAttributes = [crododile, dog, cat, santtu]
    question = question.replace('?','').lower()
    searchTerms = question.split(" ")
    animalTypes = []
    answer = 'I don\'t know'
    animalCharacters = {}
    term = ''
    #print('terms == '+str(searchTerms))
    for a in animalAttributes:
        animalTypes.append(a.get('species'))
        animalCharacters[a.get('species')] = (a.get('character'))
    for s in searchTerms:
        if s[-1] == 's':
            t = len(s)-1
            term = s[0:t]
        else:
            term = s
        #print('term is == '+ term)
        if term in animalTypes:
            answer = 'Answer: ' +term + 's are ' + animalCharacters.get(term)
    print(answer)

# ---------------- INPUT ------------- #   
# animals
leo = {'name' : 'Leo', 'type' : 'cat', 'weight' : 5, 'age' : 7}
ulla = {'name' : 'Ulla', 'type' : 'dog', 'weight' : 10, 'age' : 3}
doe = {'name' : 'Doe', 'type' : 'cat', 'weight' : 2, 'age' : 1}

myAnimals = [leo, ulla, doe]

"""
# list names
printAnimalNames(myAnimals)

# calculate averages for cats
species = 'cat'
printAnimalStats(myAnimals, species)

# buy new cat
print('''
shopping more cats :D''')
jack = {'name' : 'Jack', 'type' : 'cat', 'weight' : 10, 'age' : 10}
myAnimals.append(jack)

# check new average cat stats
species = 'dog'
printAnimalStats(myAnimals, species)  

# do I have crocodiles
species = 'crocodile'
printAnimalStats(myAnimals, species)  

# ask about crocodile
print(' ')
"""
print('Question time ------>')
