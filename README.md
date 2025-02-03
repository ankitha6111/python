SYMBOLS = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz1234567890 !@#$%^&*().{[]}|'

message = input("enter ur message:")
key = input("enter ur key:")

translated = ''

for symbol in message:
    if symbol in SYMBOLS:
        symbolindex = SYMBOLS.find(symbol)
        translatedindex = symbolindex + key

        if translatedindex >= len(SYMBOLS):
            translatedindex = translatedindex - len(SYMBOLS)

        translated += SYMBOLS[translatedindex]
    else:
        translated += symbol

print("Encrypted message:", translated)
