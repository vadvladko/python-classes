# python-classes
Hello
#классы
class Animals():

  def __init__(self, view, name, weight, voice, actions1):
    self.view = view
    self.name = name
    self.weight = weight
    self.voice = voice
    self.actions1 = actions1

  
class Birds(Animals):
  def __init__(self, view, name, weight, voice, actions1, actions2):
    super().__init__(view, name, weight, voice, actions1)
    self.actions2 = actions2
  
  def show_animals(self):
    description_1 = (self.view, 'Имя животного: ' + self.name, 'Вес животного (кг): ' + str(self.weight), 'Голос животного: ' + self.voice, 'Действие 1: ' + str(self.actions1), 'Действие 2: ' + str(self.actions2))
    
    print(description_1)

class Milk(Animals):
  def __init__(self, view, name, weight, voice, actions1, actions2):
    super().__init__(view, name, weight, voice, actions1)
    self.actions2 = actions2
  
  def show_animals(self):
    description_2 = (self.view, 'Имя животного: ' + self.name, 'Вес животного (кг): ' + str(self.weight), 'Голос животного: ' + self.voice, 'Действие 1: ' + str(self.actions1), 'Действие 2: ' + str(self.actions2))
    
    print(description_2)  

class Wool(Animals):
  def __init__(self, view, name, weight, voice, actions1, actions2):
    super().__init__(view, name, weight, voice, actions1)
    self.actions2 = actions2
  
  def show_animals(self):
    description_3 = (self.view, 'Имя животного: ' + self.name, 'Вес животного (кг): ' + str(self.weight), 'Голос животного: ' + self.voice, 'Действие 1: ' + str(self.actions1), 'Действие 2: ' + str(self.actions2))
    
    print(description_3)  


gus1 = Birds('Гусь', 'Серый', 5, 'Га-га', 'кормить', 'собрать яйца')
gus2 = Birds('Гусь', 'Белый', 8, 'Га-га', 'кормить', 'собрать яйца')
utka = Birds('Утка', 'Кряква', 3, 'Кря-кря', 'кормить', 'собрать яйца')
kurica1 = Birds('Курица', 'КоКо', 2, 'Ко-ко', 'кормить', 'собрать яйца')
kurica2 = Birds('Курица', 'Кукареку', 2.5, 'Ко-ко', 'кормить', 'собрать яйца')
korova = Milk('Корова', 'Манька', 570, 'Му', 'кормить', 'надоить молоко')
koza1 = Milk('Коза', 'Рога', 75, 'Ме-ме', 'кормить', 'надоить молоко')
koza2 = Milk('Коза', 'Копыта', 82, 'Ме-ме', 'кормить', 'надоить молоко')
ovca1 = Wool('Овца', 'Барашек', 74, 'Бе-бе', 'кормить', 'стричь шерсть')
ovca2 = Wool('Овца', 'Кудрявый', 80, 'Бе-бе', 'кормить', 'стричь шерсть')

gus1.show_animals()
gus2.show_animals()
utka.show_animals()
kurica1.show_animals()
kurica2.show_animals()
korova.show_animals()
koza1.show_animals()
koza2.show_animals()
ovca1.show_animals()
ovca2.show_animals()

animals_dict = {
  gus1.name: gus1.weight, 
  gus2.name: gus2.weight, 
  utka.name: utka.weight,
  kurica1.name: kurica1.weight,
  kurica2.name: kurica2.weight,
  korova.name: korova.weight,
  koza1.name: koza1.weight,
  koza2.name: koza2.weight,
  ovca1.name: ovca1.weight,
  ovca2.name: ovca2.weight,
        }

print('Общий вес животных:', sum(animals_dict.values()), 'кг')

print('Самое тяжелое животное - ', max(animals_dict.items(), key = lambda k: k[1]), 'кг')
