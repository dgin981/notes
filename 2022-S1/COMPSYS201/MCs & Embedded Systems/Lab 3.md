```C
void bitEnable(int address, int bit) {
	address |= 1 << bit;
}

void bitDisable(int address, int bit) {
	address &= ~(1 << bit);
}

int bitGet(int address, int bit) {
	return (address & (1 << bit)) > 0; // >0 normalisation to 1/0
}
```