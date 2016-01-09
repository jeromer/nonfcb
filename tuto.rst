======================================
Comment désactiver le NFC sur votre CB
======================================

.. contents::

Pourquoi vouloir désactiver ce système ?
----------------------------------------

Les arguments qui reviennent souvent sont:

- c'est pas sécurisé
- c'est pas sécurisé
- c'est pas sécurisé
- c'est pas sécurisé
- c'est pas sécurisé
- ma banque vous a livrée votre nouvelle CB avec le NFC en disant un truc du
  genre :

    Nous ne fournissons plus de carte bleue sans technologie sans contact, mais
    vous pouvez désactiver le système dans votre interface de gestion de compte
    sur http://blablabla.com/bullshit. Le système sans contact est très
    sécurisé. Vous comprendrez que notre banque BigMoneyDuContribuable ne se
    permettrait pas de mettre en service un système non sécurisé.

Y'a quoi sur ma CB en fait ?
----------------------------

Sur votre CB, vous avez en théorie:

- une puce (recto): utilisée pour le paiement chez les commerçants

- une bande magnétique (verso): utilisée pour vos retraits d'argent, les péages, et aussi pour les paiements
  ou la puce n'est pas utilisée, quand vous partez à l'étranger par exemple

.. Warning::

    Lors de la désactivation du NFC, il ne faut surtout PAS toucher à la puce
    au recto, ni à la bande magnétique au verso.


Désactivation
-------------

Matériel nécessaire
+++++++++++++++++++

- une lampe torche, à défaut une lampe de poche assez puissante
- un cutter avec une lame neuve idéalement

Manipulation
++++++++++++

.. Note::

    Je ne suis pas certain que le format de circuit NFC soit le même pour
    toutes les banques/types de carte. En conséquence, ce qui peut marcher sur
    une carte X et une marque Y peut ne pas marcher pour une autre banque ou un
    autre type de carte.

Alors en fait, c'est relativement simple. Il suffit de tenir sa carte bleue,
côté "recto" face à vous, et de passer la lampe sur le verso de la carte.

Vous devriez voir les circuits intégrés à la carte. Par exemple, si vous mettez
la lampe derrière la puce, vous devriez voir le circuit qui rentre et sort de
la puce. Surtout ne pas y toucher ;)

Baladez la lampe sur tout le verso de la carte, avec un peu de chance vous
devriez voir un circuit, avec plusieurs fils parallèles qui effectue le tracé
décrit ci-dessous: ::


      +--------------------------------------------------------+
      |xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx  |
      +x----------------------------------------------------x--+
      |x            bande magnétique au verso               x  |
      +x----------------------------------------------------x--+
      |x                                                    x  |
      |x +-------+                                          x  |
      |xx|       |                                          x<-----------------+
      | x|puce   +xxxxxx                                    x  |               +
      |  |       |   xxx                                   xx  |              NFC
      |  +-------+      xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx    |
      |                                                        |
      |                                                        |
      +--------------------------------------------------------+


Si vous voyez ce genre de tracé, il suffit de mettre un coup de cutter à un
endroit éloigné de la puce et de la bande magnétique.

Personnellement, j'ai coupé ici: ::

      +--------------------------------------------------------+
      |xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx  |
      +x----------------------------------------------------x--+
      |x            bande magnétique au verso               x  |
      +x----------------------------------------------------x--+
      |x                                                    x  |
      |x +-------+                                          x  |
      |xx|       |                                          x  |
      | x|puce   +xxxxxx                                    x  |
      |  |       |   xxx                                   xx  |
      |  +-------+  |   xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx    |
      |             |                                          |
      |             |                                          |
      +-------------|------------------------------------------+
                    |
      ici ----------+

Mais ici, ça devrait aussi marcher, tout vous ne touchez PAS à la carte
magnétique de la CB: ::

      +--------------------------------------------------------+
      |xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx  | <--- par là
      +x----------------------------------------------------x--+
      |x            bande magnétique au verso               x  |
      +x----------------------------------------------------x--+
      |x                                                    x  | <--- ou par là
      |x +-------+                                          x  |
      |xx|       |                                          x  |
      | x|puce   +xxxxxx                                    x  |
      |  |       |   xxx                                   xx  |
      |  +-------+      xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx    |
      |                                                        |
      |                                                        |
      +--------------------------------------------------------+

En exemple, voici 2 de mes cartes bleues:

Crédit Mutuel
~~~~~~~~~~~~~

**Visa**

    ..image:: img/cm-visa.jpg

**Master Card**

    ..image:: img/cm-mastercard.jpg

Sources intéressantes
---------------------

- http://www.lesclesdelabanque.com/Web/Cdb/Particuliers/Content.nsf/DocumentsByIDWeb/8scm8w
- http://www.cnetfrance.fr/news/securite-le-nfc-une-vraie-passoire-39797541.htm
- https://en.wikipedia.org/wiki/Near_field_communication
- http://jonathan.lalou.free.fr/?p=2127
- http://www.panoptinet.com/cybersecurite-pratique/comment-neutraliser-le-nfc-sur-sa-carte-bancaire/
