# Nastavení SSH v Gitu

_Tento návod je určen pro Windows. Pro mac a Linux by byl návod téměř totožný, lišit se bude akorát cesta k Public key_

V jakémkoliv příkazovém řádku - cmd/powershell - napište následující příkaz (email zvolte stejný, kterým jste se registrovali na Githubu)

```
ssh-keygen -t ed25519 -C "tvuj_mail@priklad.cz"
```

Vyskočí na vás tato hláška - stiskněte ENTER

```
> Generating public/private ed25519 key pair.
> Enter file in which to save the key (C:\Users\Jmeno/.ssh/id_nejakecislo):
```

Vyskočí nová hláška o zadání passphrase (jedná se o heslo k SSH klíči - pro lepší zabezpečení můžete vyplnit, ale není nutně potřeba) - pro zjednodušení práce nemusíte heslo vyplňovat, jen stistkněte ENTER:

```
> Enter passphrase (empty for no passphrase):
```

Podobná hláška znovu, opět ENTER

```
> Enter same passphrase again:
```

**Tím jsme vytvořili pár klíčů: Public key a Private key**

_Private key zůstává na vašem počítači a s nikým ho nesdílíte. Public key nahrajeme na Github a pomocí něj budeme ověřovat připojení_

Klíče bydlí ve složce C:\Users\\**Jmeno**\\.ssh (Jmeno je vaše jméno ve Windows), kam se přesuneme v příkazovém řádku pomocí

```
cd C:\Users\Jmeno\.ssh
```

Zkontrolujeme název klíče

```
dir
```

Pomocí notepadu otevřeme náš Public key, který má koncovku .epub

```
notepad id_nejakecislo.epub
```

Číslo z notepadu zkopírujeme (Ctrl+C) a otevřeme si Github

V Githubu klikneme vpravo nahoře na naší ikonu

![image](https://gist.github.com/assets/84028625/5b148de4-7eb6-4ecb-9a3c-a4502049b535)

Settings

![image](https://gist.github.com/assets/84028625/744bdf9c-2d2e-4e70-afbb-ebd8d6ea5a96)

V levé části SSH and GPG keys

![image](https://gist.github.com/assets/84028625/d579478d-0342-4311-a092-eabe979095c6)

Vpravo nahoře New SSH key

![image](https://gist.github.com/assets/84028625/d4ad51bf-9459-4461-8cf9-dc4eb24d65a2)

Do title napsat cokoliv, do pole Key nakopírovat náš Public key a kliknout na Add SSH key

![image](https://gist.github.com/assets/84028625/801042c8-6f11-4172-a5fd-130d0c507d6c)

Hotovo. Nyní můžete používat SSH připojení a nemusíte ověřovat přihlašování přes prohlížeč.

Při klonování repozitářů nyní budete volit SSH

![image](https://gist.github.com/assets/84028625/164027f4-57ab-4bf2-aa10-a81c97c7b674)
