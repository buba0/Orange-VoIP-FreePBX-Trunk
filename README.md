# [Instructions in English 🇬🇧/🇺🇸](README_en.md) <--- Click here
# Jak dodać telefon domowy Orange do FreePBX jako trunk

Wraz z światłowodem często dostajemy telefon domowy w ramach pakietu Orange LOVE. Telefon ten jest oparty na technologii VoIP więc technicznie nie musi być dostępny tylko na FunBoxie.

---

### 1. Otrzymanie danych VoIP
Aby cokolwiek zrobić z tym telefonem musimy mieć do niego dane logowania. Dane możemy uzyskać na infolinii, należy poprosić o dane logowania do neofonu.

Dane otrzymamy mailem lub SMSem, będą one miały format `48xxxxxxxxx@neofon.tp.pl`, gdzie `xxxxxxxxx` to nasz numer telefonu, oraz hasło które oczywiście dla każdego jest inne.

---

### 2. Dodanie trunka w FreePBX
Wchodzimy w `Connectivity` ---> `Trunks` i uzupełniamy jak na obrazkach

![1.png](images/pl/1.png)
![2.png](images/pl/2.png)
### Notatka 
Jeżeli korzystasz z Funboxa a nie z własnego routera, telefon nie będzie działać, lub będzie działać do czasu do kiedy Orange nie wypuści nowej konfiguracji do Funboxa. W takim przypadku w "Auth username" należy wpisać numer telefonu w formacie `48xxxxxxxxxa@neofon.tp.pl` (z dopiskiem a na końcu).

Jeśli dalej nie działa to należy wejść w zakładkę "Advanced" i wkleić w pole "AOR Contact" wartość w formacie `sip:48xxxxxxxxxa@neofon.tp.pl:5060` (numer telefonu z dopiskiem "a"), i w pole "Match (Permit)" wartość `83.0.8.0/24`

![3.png](images/pl/3.png)
![4.png](images/pl/4.png)

---

### 3. Inbound route dla trunka

Wchodzimy w `Connectivity` ---> `Inbound Routes` i uzupełniamy jak na obrazkach

![5.png](images/pl/5.png)
![6.png](images/pl/6.png)

---

### 4. Outbound route dla trunka

Wchodzimy w `Connectivity` ---> `Outbound Routes` i uzupełniamy jak na obrazkach

![7.png](images/pl/7.png)

![8.png](images/pl/8.png)

Przygotowałem dial patterns dla (chyba) wszystkich numerów publicznych w Polsce, które możemy importować. [Pobierz](files/dial_pattern.csv)

![9.png](images/pl/9.png)

![10.png](images/pl/10.png)

---

### Kontakt
Jeśli macie jakieś pytania proszę kierować je na adres mailowy: [jakub.bednarczyk@mail.buba.net.pl](mailto:jakub.bednarczyk@mail.buba.net.pl).

Lub otworzyć [GitHub issue](https://github.com/buba0/Orange-VoIP-FreePBX-Trunk/issues).

&copy; 2026 [buba.net.pl](https://buba.net.pl)


## Star History

<a href="https://www.star-history.com/#buba0/Orange-VoIP-FreePBX-Trunk&type=date&legend=top-left">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=buba0/Orange-VoIP-FreePBX-Trunk&type=date&theme=dark&legend=top-left" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=buba0/Orange-VoIP-FreePBX-Trunk&type=date&legend=top-left" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=buba0/Orange-VoIP-FreePBX-Trunk&type=date&legend=top-left" />
 </picture>
</a>
