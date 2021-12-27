# XOR-i
For the following ciphertext, the clue is to use the XOR operation:

`4d 40 41 50 7f 4c 21 6a 28 65 63 60 69 2d 6f 61 30 49 5d 41 34 72 77 63 7d 39 53 3b 70 74 6a 7a 52 40 4e 4f 5d 5 45 46 46 e 5e b 49 5b 4b 41 4d`

Using the known string format for flags:
- 4d -> 4d (M)
- 40 -> 41 (A)
- 41 -> 43 (C)
- 50 -> 53 (S)
- 7f -> 7b ({)

Doing some XOR operations reveals that for each character, the XOR operation is different, the value that needs to be XORed is the index in which the character appears in. For example:

- 4d ^ 0x0 -> 4d
- 40 ^ 0x1 -> 41
- 41 ^ 0x2 -> 43
- 50 ^ 0x3 -> 53
- 7f ^ 0x4 -> 7b

Do this for the rest of the ciphertext. In Java:

`int[] arr = {77, 64, 65, 80, 127, 76, 33, 106, 40, 101, 99, 96, 105, 45, 111, 97, 48, 73, 93, 65, 52, 114, 119, 99,	125, 57, 83, 59, 112, 116, 106, 122, 82, 64, 78, 79, 93, 5, 69, 70, 70, 14, 94, 11, 73, 91, 75, 65, 77};
		for (int i = 0; i < arr.length; i ++) {
			arr[i] = arr[i] ^ i;
			System.out.print((char) arr[i]);
		}
		System.out.println();`

The flag is `MACS{I'm like an XOR gate I literally can't even}`
