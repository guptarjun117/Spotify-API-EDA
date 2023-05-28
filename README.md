# Spotify-API-EDA
**Performing Exploratory Data Analysis using the Spotify API to gain some interesting insights using the Audio Features stats!**
https://developer.spotify.com/documentation/web-api/reference/get-audio-features

**Audio Features are refered to a set of descriptive attributes or characteristics of a particular audio track, album or the artist as a whole.**

**Danceability** - Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable.

**Energy** - Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach prelude scores low on the scale. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy.

**Speechiness** - Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value. Values above 0.66 describe tracks that are probably made entirely of spoken words. Values between 0.33 and 0.66 describe tracks that may contain both music and speech, either in sections or layered, including such cases as rap music. Values below 0.33 most likely represent music and other non-speech-like tracks.

**Acousticness** - A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic.

**Instrumentalness** - Predicts whether a track contains no vocals. "Ooh" and "aah" sounds are treated as instrumental in this context. Rap or spoken word tracks are clearly "vocal". The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content. Values above 0.5 are intended to represent instrumental tracks, but confidence is higher as the value approaches 1.0.

**Valence** - A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry).

**Time Signature** - An estimated time signature. The time signature (meter) is a notational convention to specify how many beats are in each bar (or measure). The time signature ranges from 3 to 7 indicating time signatures of "3/4", to "7/4".

----

# **Insight 1:**

Comparing original released metal albums with their re-released "Remastered" counterparts.
Release of remastered albums is a hit or miss in the metal community. Either it will improve the quality if the orignal songs were poorly produced in the first place or decreased the quality of already well-produced song. Or, nothing.
Many such cases, like Metallica's Black Album (Metallica) was already a masterpiece in terms of production released in 1991. But its Remastered re-release in 2021 was literally no change to the quality for many. How does Spotify see the change between those two albums?




Album Name: Metallica (1991)

Mean Audio Features:

* danceability: 0.5546666666666665
* energy: 0.78825
* speechiness: 0.03573333333333333
* acousticness: 0.006583250000000002
* instrumentalness: 0.09707075166666666
* valence: 0.4318333333333333
* time_signature: 3.9166666666666665

![image](https://github.com/guptarjun117/Spotify-API-EDA/assets/105283893/4ca95aaf-2e05-418c-9a81-5e58a3dd0b86)



Album Name: Metallica (Remastered 2021)

Mean Audio Features:

* danceability: 0.5390833333333332
* energy: 0.8115
* speechiness: 0.038483333333333335
* acousticness: 0.008321166666666666
* instrumentalness: 0.051892200833333346
* valence: 0.42524999999999996
* time_signature: 3.9166666666666665

![image](https://github.com/guptarjun117/Spotify-API-EDA/assets/105283893/efd088f5-7fdd-4fee-993a-469470d77492)


So there are changes, but very minute. Maybe it would be better to test this in the case where the remastered album does actually change different from the original.

----

# **Insight 2:**

It is well known that metal bands cannot truly stick a single type of sound that they were well known for once. For example, my favourite Melodic Death Metal band, In Flames. Since its birth in 1993, it has changed **a lot** over the years up till now. Even creating a division in the fan base because there fans who like different timeline/sounds of the band. But how does the Spotify's Audio Features consider these changes? Negligible or some major changes?

In Flames' discography:
* Lunar Strain (1994)
* Subterranean (1995)
* The Jester Race (1996)
* Whoracle (1997)
* Colony (1999)
* Clayman (2000)
* Reroute To Remain (2002)
* Soundtrack To Your Escape (2004)
* Come Clarity (2006)
* A Sense of Purpose (2008)
* Sounds of a Playground Fading (2011)
* Siren Charms (2014)
* Battles (2016)
* I, The Mask (2019)
* Foregone (2023)


---


Album Name: Lunar Strain

Mean Audio Features:
* danceability: 0.272
* energy: 0.7542
* speechiness: 0.063
* acousticness: 0.165760698
* instrumentalness: 0.102137707
* valence: 0.33324
* time_signature: 3.8

![image](https://github.com/guptarjun117/Spotify-API-EDA/assets/105283893/246d00ae-ec5c-429c-8980-b18a2bd464a4)

---

Album Name: Subterranean

Mean Audio Features:
* danceability: 0.27385714285714285
* energy: 0.876
* speechiness: 0.07379999999999999
* acousticness: 0.1256252142857143
* instrumentalness: 0.5546269999999999
* valence: 0.29071428571428576
* time_signature: 4.0

![image](https://github.com/guptarjun117/Spotify-API-EDA/assets/105283893/86454ad6-668e-4860-8930-fa83a4486c29)

---

Album Name: The Jester Race (Black Ash-Inheritance Version)

Mean Audio Features:
* danceability: 0.3226428571428572
* energy: 0.9030714285714285
* speechiness: 0.07986428571428572
* acousticness: 0.061999595000000005
* instrumentalness: 0.8290714285714283
* valence: 0.4200714285714286
* time_signature: 3.642857142857143

![image](https://github.com/guptarjun117/Spotify-API-EDA/assets/105283893/bc16a7b1-e459-4a2f-be8e-c3b29f77155e)

---

Album Name: Whoracle

Mean Audio Features:
* danceability: 0.4636666666666666
* energy: 0.9629166666666666
* speechiness: 0.07943333333333333
* acousticness: 0.00892556
* instrumentalness: 0.7214916666666666
* valence: 0.38166666666666665
* time_signature: 3.75

![image](https://github.com/guptarjun117/Spotify-API-EDA/assets/105283893/62fdb3fc-d0e1-4a3a-b34a-d40cc5d7fb80)

---

Album Name: Clayman

Mean Audio Features:
* danceability: 0.3996923076923077
* energy: 0.9072307692307692
* speechiness: 0.06495384615384614
* acousticness: 3.2476153846153846e-05
* instrumentalness: 0.690846153846154
* valence: 0.45184615384615384
* time_signature: 3.923076923076923

![image](https://github.com/guptarjun117/Spotify-API-EDA/assets/105283893/91209c46-de2d-49b5-8379-094b43000b5f)

---

Album Name: Reroute to Remain

Mean Audio Features:
* danceability: 0.4327142857142857
* energy: 0.9425714285714285
* speechiness: 0.06343571428571429
* acousticness: 8.363e-05
* instrumentalness: 0.7725857142857143
* valence: 0.33297142857142864
* time_signature: 3.9285714285714284

![image](https://github.com/guptarjun117/Spotify-API-EDA/assets/105283893/e72b550e-2233-4f07-99dc-79052f9a7af2)

---

Album Name: Soundtrack to Your Escape (The Quiet Place Version)

Mean Audio Features:
danceability: 0.4927857142857142
energy: 0.9484285714285713
speechiness: 0.08629285714285714
acousticness: 0.053899955
instrumentalness: 0.7222857142857143
valence: 0.26067142857142855
time_signature: 3.9285714285714284


![image](https://github.com/guptarjun117/Spotify-API-EDA/assets/105283893/4c5a7108-095a-4973-97a5-90453dc0c951)

---

Album Name: Come Clarity

Mean Audio Features:
* danceability: 0.405
* energy: 0.9436923076923077
* speechiness: 0.1281923076923077
* acousticness: 0.01888747
* instrumentalness: 0.434676923076923
* valence: 0.1354923076923077
* time_signature: 4.0

![image](https://github.com/guptarjun117/Spotify-API-EDA/assets/105283893/dfee0ccf-64f1-47ea-b6f3-ce16f7ade23a)

---

Album Name: A Sense of Purpose (The Mirror's Truth Version)

Mean Audio Features:
* danceability: 0.4726
* energy: 0.9533999999999999
* speechiness: 0.07518666666666668
* acousticness: 0.004015694666666667
* instrumentalness: 0.07282722
* valence: 0.24133333333333337
* time_signature: 4.0


![image](https://github.com/guptarjun117/Spotify-API-EDA/assets/105283893/3a41acc2-f39b-4d0a-b12b-8023c8f1f0d0)

---

Album Name: Sounds Of A Playground Fading

Mean Audio Features:
* danceability: 0.47661538461538466
* energy: 0.8778461538461537
* speechiness: 0.06644615384615384
* acousticness: 0.043860371538461534
* instrumentalness: 0.18215153846153848
* valence: 0.35946923076923076
* time_signature: 4.0

![image](https://github.com/guptarjun117/Spotify-API-EDA/assets/105283893/4609eb39-82ee-49d7-9c7d-5ebc23a22ad4)

---

Album Name: Siren Charms

Mean Audio Features:
* danceability: 0.507909090909091
* energy: 0.8845454545454546
* speechiness: 0.06679090909090908
* acousticness: 0.0011901454545454543
* instrumentalness: 0.07080714545454544
* valence: 0.39001818181818176
* time_signature: 3.909090909090909

![image](https://github.com/guptarjun117/Spotify-API-EDA/assets/105283893/ae85e57d-ed90-4cd7-9e96-eae99846c86d)

---

Album Name: Battles

Mean Audio Features:
* danceability: 0.48778571428571427
* energy: 0.9124285714285716
* speechiness: 0.07959999999999999
* acousticness: 0.003505478571428571
* instrumentalness: 0.1304470721428571
* valence: 0.3180714285714285
* time_signature: 3.857142857142857

![image](https://github.com/guptarjun117/Spotify-API-EDA/assets/105283893/17e2f4a3-8687-4c69-8c7a-c6afca1e7a6a)

---

Album Name: I, the Mask

Mean Audio Features:
* danceability: 0.5094166666666667
* energy: 0.9378333333333333
* speechiness: 0.0733
* acousticness: 0.00019273333333333335
* instrumentalness: 0.01147199
* valence: 0.266
* time_signature: 4.0

![image](https://github.com/guptarjun117/Spotify-API-EDA/assets/105283893/c03655ee-acba-4cd2-94e4-5048b1ff1c8e)

---

Album Name: Foregone

Mean Audio Features:
* danceability: 0.43724999999999997
* energy: 0.8953333333333334
* speechiness: 0.09656666666666668
* acousticness: 0.04927028249999999
* instrumentalness: 0.13359666666666667
* valence: 0.2570833333333334
* time_signature: 3.6666666666666665


![image](https://github.com/guptarjun117/Spotify-API-EDA/assets/105283893/d6c1c0fa-9c8f-4b93-be5c-aebf76082e0b)
