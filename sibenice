# word game sibenice
import random


def ask_letter(count):
    letter = input(f'You have {count} attepmts. Guess one letter: ').lower()
    return letter


def change_blind(word_to_list_blind, word_to_list, letter):
    while letter in word_to_list:
        letter_index = word_to_list.index(letter)
        word_to_list_blind[letter_index] = letter
        word_to_list[letter_index] = '#'
    return word_to_list_blind


def sibenice(words: list):
    my_sep = '.' * 71
    word = random.choice(words).lower()
    word_to_list = list(word)
    word_to_list_blind = ['_'] * len(word)
    count = min(len(word) + 5, int(len(word) * 1.6), 15)
    print(my_sep)
    print('You have total', count, 'attempts to guess one word. Only lowercase. Good LUCK')
    print(my_sep)
    print(' '.join(word_to_list_blind))
    while count:
        letter = ask_letter(count)
        if letter in word_to_list:
            word_to_list_blind = change_blind(word_to_list_blind, word_to_list, letter)
        print(my_sep)
        print(' '.join(word_to_list_blind))
        if word_to_list_blind == list(word):
            return print(my_sep, '\nBravo. You are WINNER')
        count -= 1
    return print(my_sep, '\nSorry. Game is over...\n It was ', word.upper())


sibenice([
    'Faith', 'confidence', 'concept', 'cumulative', 'context', 'belief', 'doctrines', 'Religious', 'degree', 'Stage',
    'Synthetic', 'information', 'personification', 'knowledge', 'teacher', 'Jesus', 'God', 'Sabbath', 'country',
    'weekend', 'benefits', 'administration', 'damage', 'unemployment', 'example', 'public', 'election',
    'pneumonoultramicroscopicsilicovolcanoconiosis', 'hangman', 'aircraft', 'airbase', 'python', 'apple', 'car'
