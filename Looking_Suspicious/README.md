# Looking Suspicious

Category: OSINT/RECON

After a few nervous minutes, the lock gives in. You open the door and notice that it’s on the alarm. A slight chill rolls through your body from top to bottom; somewhere around the ankles it has turned into a full-scale avalanche of dread. Because if anyone sees you here, it’s literally game over. There’s no way you can stay here for more than a minute.

You run around the apartment looking for any clues, and in desperation, you go into the last room and find a piece of paper on the table.

## Solution

The entire challenge consists of finding hidden clues in the picture given.
These clues are then entered into the website: (https://lookingsus.q.2024.ugractf.ru/8t0hidr9fv0crphv)
The Username and Password are given in plain sight.

![image](https://github.com/kua23/UgraCTF/assets/61975172/6189295a-fd75-4c46-9387-7d7c3fc4e0dc)

![image](https://github.com/kua23/UgraCTF/assets/61975172/6b5fd734-9ea6-451e-8247-279005920309)

`Password: qV*!2@x>Tp{`

The phone number had to be zoomed in on and I had to do some guesswork in order to get it.
Phone Number: ![image](https://github.com/kua23/UgraCTF/assets/61975172/6f7e2fef-508a-4e59-a160-33e66021162e)
![image](https://github.com/kua23/UgraCTF/assets/61975172/6a6847a4-1c31-4681-9852-2ca74599fc5c)

As there is no phone in the picture, I entered 000000 as I could not receive any OTP.
![image](https://github.com/kua23/UgraCTF/assets/61975172/49750683-db38-40ac-a94d-eb4edab298d0)


In order to find the last four digits of the credit card, I first converted the image to LSB Half which is used to transparent hide an image in another image using [this tool](https://georgeom.net/StegOnline/upload).

![image](https://github.com/kua23/UgraCTF/assets/61975172/50b1355d-5c2e-4cb4-8a9e-7554307b6666)

This is where I left the challenge, however, the passport number could be found too.

`Passport number: 0692`

![image](https://github.com/kua23/UgraCTF/assets/61975172/9359028e-0c1f-41cb-ae2a-4e7639128742)
Here, 9 and 2 can be found by checking out the laser-printed numbers of the passport in Google.

For the name of the company I work in, the pen contains the information.

  ![image](https://github.com/kua23/UgraCTF/assets/61975172/cf56eb48-0690-4f69-b3b7-d43e39921048)

For the name of the country last visited, the answer is India as there are Rupees present on the table.

![image](https://github.com/kua23/UgraCTF/assets/61975172/e873356a-0428-4d7e-9ad5-89866a117cf3)

And lastly, for the Credit Card Number it is `5321304698557524`
How we can find this out is, we know the last 8 numbers, that is `98557524`. In order to find out the first 6 numbers, we can search for the card which in this case is a Rocketbank Mastercard as every first 6 letters of the card are usually the same. This can be done using Ynadex. For the 7th number, we can use the Luna Algorithm to find it out, which then gives us 4.
Thus, we get the answer and then the flag.

### Flag
`ugra_sometimes_you_just_narrowly_escape_and_win_g4sihnm99qlf`








