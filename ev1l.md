# ev1l
Cipher text: 153 129 132 165 245 240 95 232 189 102 226 101 189 101 235 96 215 249
The known format for plaintext is something like "MACS{...}", so:
- 153 corresponds to decimal ASCII 77 (M)
- 129 corresponds to decimal ASCII 65 (A)
- 132 corresponds to decimal ASCII 67 (C)
- 165 corresponds to decimal ASCII 83 (S)
- 245 corresponds to decimal ASCII 123 ({)
- 249 corresponds to decimal ASCII 125 (})

There is a very simple pattern that emerges, the formula for decoding each value, where y is the plaintext and x is the ciphertext:
`y = (int) x/2 + 1`

Decoding every value gives:
`7 65 67 83	123	121	48 117 95 52 114 51 95 51 118 49 108 125`

Converting this to ASCII gives:
`MACS{y0u_4r3_3v1l}`
