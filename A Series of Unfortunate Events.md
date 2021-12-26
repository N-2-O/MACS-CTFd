# A Series of Unfortunate Events
Download the image and view in a hex editor. At the end of the file is a clue:
> I hope you have watched the film recently, It's one of my childhood favourites... 
> Hoping you can bring out your inner "Klaus" and solve this series of unfortunate srehpic...
> ==QIzJXYllHIwAzMgIXZ29GIy9mZgUGbiF2ahVmci5WdgMXY3BCdJBiLu4iclhGcpNGIzlGa0BSZkFWbgkXdnBCaj5WZyZGIl12bTBiLs9WcgEnZjtme5RGI5JHbgU2ZzBSZktmaiBHZjNnagU2bzpXYlV2YgcnY0BCZzBydslGb2dHe1xGT

Notice that "ciphers" is spelt backwards and that the last line looks like it is base64 encoded but backwards. Reverse the text then decode it using base64, ending up with:
> Lluxwvlilw sd tbw ceeazsoe jscdpbjkde sge lry dyzkcfq qol. Some french guy made this cipher... It was unbreakable for over 300 years!

The clue points to the cipher being a Vigenere cipher. Decoding the ciphertext will give:
> Baudelaire is the steghide passphrase you are looking for
