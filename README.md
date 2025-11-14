# Konspekt
```csharp
namespace MinuKonspekt
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine(/*abc*/"hapukapsas");
            // "Console"   -> on moodul C# mida me adresserime, Console aitab teha tegevusi käsureal
            //             -> näitab, et meil on vaja adresseerida mingisugust funktsiooni või meetodit mooduli "Console" seest.
            // "WriteLine" -> Funktsioon mida me parasjagu kasutame.
            // ()          -> sulupaar mis omab funktsiooni tööks vajalikku infot
            // []          -> tähistab massiive
            // {}          -> koodiplokk, tavaliselt kas pärast (if, else if) tingimust, namespace'i või funktsiooni kirjeldust
            // "hapukapsas"-> parameeter mis antakse funktsioonile WriteLine töötlemiseks kaasa.
            //              //    -> Taane aitab arendajal aru saada, kuskohas millise koodiploki sees kood asub, see on vajalik ka kompilaatorile samal eesmärgil.
            //             -> kõik koodilause lõppevad komakooloniga, mis tähistavad lause lõppu
            //             -> tähistab üherealist kommentaari
            // /**/        -> tähistab mitmerealist kommentaari või kommentaariregiooni

            int muutuja = 3;
            // int         -> on muutuja nime ees olev andmetüübi kirjaldus mis näitab ära, millist
            //                tüüpi andmed selle muutuja sees on.
            // "muutuja"   -> on nimetus, ehk muutuja, mis noiab endas mingeid sndmeid, inimloetava
            //                sõnaga, ja mille abil saab neid addresseerida koodi sees.
            // =           -> üksik võrdsmärk omistab muutuja sisse vastava vääruse mis asub 
            //                teiselpool võrdusmärki.
            // 3           -> muutujale omistatav väärtus.

            /* Võimalikud andmetüübid mida vaja võib minna: */
            int a = 1; // int on täisarv
            decimal b = 2.1M; // desimal on kümnendsüsteemis olev komakohaga arv
            float c = 3.9f; //float on 32-biitine komakohaga arv
            double d = 5.6d; // double on 64-bitine komakohaga arv
            char cl = 'a'; // üksainus täht või tähemark mis asub ülakomadde vahel 
            string s = "tekst"; //tähtedest koosnev sõna või tekast, tähistatakse jutmärkidega ""
            var X = "abc"; //var on ebamäärase andmetüübiga kohalik muutuja 
            var y = 123;   //ta võib omada endas teisi andmetüüpi
            const int z = 9; // konstant-tüüpi muutujaid ei saa muuta, nende sise on read-only


            /* Võimalikud andmetüübid mida vaja võib minna: */
            int a = 1; // integer on täisarv
            decimal b = 2.1M; // decimal on kümnendsüsteemis olev komakohaga arv
            float c = 3.9f; // float on 32-bitine komakohaga arv
            double d = 5.6d; // double on 64-bitine komakohaga arv
            char e = 'a'; // üksainsa tähe või tähmärgi märk tähistakse ülakomadga ''
            string s = "tekst"; // tähtedest koosnev sõna või tekst, tähistatakse jutumärkidega ""
            var x = "abc"; // var on ebamäärase andmetüübiga kohalik muutuja
            var y = 123; // ta võib omada endas erineisi andmetüüpe
            const int z = 9; // konstant-tüüpi muutujaid ei saa muuta, nende sisu on read-only

            /* Võimalikud komposiitandmetüübid */
            // 1. massiiv
            // [] - > Massiiv on komposiitandmetüüp, mille sees saab olla mitmeid samat tüüpi lihtandmeid. Massiivi tähistatakse kantusulgudega.
            //        Massiivse saab olla ükskõik millist lihtandmetüüpi massiiv.
            //        Massiivi tekitamisel tuleb ära öelda kui pikk või kui suur see massiiv on.
            //        Massiiv ei pea olema koostatud ainult lihtandmetüüpidest, vaid massiive saab olla ka tehtud teistest komposiitandmetüüpidest
            //        Sealhulgas massiiv ise.

            // Esimene tekitusviis:
            int[] arvuMassiiv = new int[3];   // andmetüüp int väljendab et tegu on täisarvutüüpi andmega ja kantusulgud väljendavad et
                                              // tegu ka massiiviga, muutuja nimeks on "arvuMassiiv" ja võrdusmärgi abil on omistatud
                                              // muutuja sisse uus tühi massiiv kasutades kaitstud sõna "new", millele järgneb selle massiivi andmetüüp ja pikkuse sätestus "int[3]".
                                              // See tähendab et siin massiivis on 3 elementi, mis on täisarvud.
            // Teine tekitusviis:
            int[] arvuMassiiv2 = { 1, 2, 3 }; // teine massiivi tekitusviis kus järjendi pikkuse sätestamise asemel, pannakse elemendid kohe
                                              // järjendit omava muutujasse sisse, järjendi pikkust sätestama ei pea, kuna pikkuse tuletab kompilaator
                                              // sinna sisse pandud elementide koguse järgi.
                                              // --- massiivi sisemised meetodid:
            
            // -- massiivi sisemised meetodid:
            int hasThisMany = arvuMassiiv.Length; // massiivi meetod "Length" mille me saame kasutusele võtta punkti abil, loendab kokku 
                                                  // mitu elementi, adresseeritav massiiv omab, omistatakse ainult järjendi pikkus, mitte 
                                                  // järjendi sees olevaid elemente.

            //2. Loend:
            // List<T> -> Loend on adnmetüüp, mille sees saab olla mitmeid samat tüüpi liht ja komposiitandmeid. Loend-tüüpi andmeid tähistatakse
            //            täiendava andetüübkirjeldusega "List" mille järel noolsulgudesse <> asetatakse mis tüüpi andmed seal loendis on.
            //            Loendi tekitamisel, erinevalt massiivist, ei pea ütlema kui pikk loend on. Loendisse saab dünaamiliselt elemente juurde lisada,
            //            ehk tema pikkus ei ole fikseeritud. Sarnaselt massiiviga saab temas hoida ka teisi loendeid.
            // Esimine tekitusviis:
            List<int> arvuNimekrii = new List<int>(); //Andmetüübi kirjeldis "List<>" näitab et tegu on loendiga. Listi noolsulgude <> vahel on loendis
                                                      //olevate andmete andmetüüp. Antud juhul on andmetüübiks "iks" mis tähistab säisarve. Muutuja enda 
                                                      //nimeks on "arvuNimekiri". Omistame sellesse muutujasse kaitsud sõna "new" abl uue tühja
                                                      //täisarvuloendi sätestusega "List<int>()".

            // Teine tekitusviis:
            List<int> arvuNimikiri2 = new List<int>() { 1, 2, 3 }; //Teine loendi tekitusviis. Andmetüübi kirjeldus "List<>" näitab et tegu on loendiga, Listi
                                                                   //noolsulgude vahel on loendis olevate elementide andmetüüp. Antud juhul on andmetüübiks "int"
                                                                   //mis tähistab täisarve. Muutuja enda nimeks on "arvuNimikiri2". Omistame selle muutujasse
                                                                   //kaitstud sõna "new" abil uue taäisarvuloendi, aga seekord, pealesätestust "List<int>()" saame
                                                                   //intsantsieerimise hetkel talle kaasa anda ka esimesi elemente. Antud juhul on need elemendid
                                                                   //"1", "2 ja "3". Elemendid sisestatakse nimekirja loogeliste sulgude vahel. Enam ei ole tegu
                                                                   //tühja nimekirjaga, vaid loendiga kus on kolm elementi juba sees.
                                                                   // kolmas tekitusviis:
            List<int> arvuNimekiri3 = new List<int>(3); //Kolmas loendi tekitusviis. Andmetüübi kirjeldus "List<>" näitab et tegu on loendiga, Listi noolsulgude
                                                        //vahel on loendis olevate elementide andmetüüp. Antud juhul on andmetüübiks "int" mis tähistab täisarve.
                                                        //Muutuja enda nimeks on "arvuNimekiri3". Omistame sellesse muutujasse kaitstud sõna "new" abil uue 
                                                        //täisarvuloendi, aga tavaliste sulgude vahele paneme arvu "3". Sarnaselt massiiviga ütleb see, et
                                                        //Loend on 3 elemndi suurune. Loend ise ja tema elemendid on tühjaad, aga seal on 3 elementi. Arv "3"
                                                        //on parameeter mida Listi konstruktor pikkuse määramiseks kasutab. Nimekiri säilitab oma omaduse muuta
                                                        //pikkust elementide lisamise-eemaldamisega, aga vajadusel saab nii anda talle pikkuse.

            int aa = 9001;
            // -- Loendu sisemised meetodid:
            arvuNimekiri3.Add(99); //Loendi meetod "Add()" lisab enne punkti olevale järjendile uue elemendi, element mdia lisatakse on Add meetodi sulgude
                                   //vahel. Elementi sasab lisada otse (antud juhul täisarv "99") 
            arvuNimekiri3.Add(aa); //või muutujane
            int loendiPikkus = arvuNimekiri3.Count(); //Loendi meetod "Count()" loeb kokkku mitu elementi järjendis on, meetod tagastab täisarvu mis vastab 
                                                      //elementide kogusele.
            bool KasSeearvOn = arvuNimekiri3.Contains(3); //Loendi meetod "Contains()", otsib kogu järjendi seest elementi, mis vastab sulgude vahel olevale
                                                          //parameetrile. Meetod tagastab kas "true" või "false" - on leitud või ei ole. Tegemist on
                                                          //põhimõtteliselt foreach tsükLiga, mis otsib kindlat vastet, töötades läbi kogu loendi.
            arvuNimekiri3.Remove(4); //Loendi meetod "Remove()"eemaldab enne olevast loendist, kindlal asukohal oleva elemendi. Sulgude vahel on parameetriks
                                     //eemaldatava elemendi asukohajärjekorranumber.














            //põhilised matemaatilised tehted
            int liitimne = 1 + 1; //liitmine, kaks arvu liidetakse kokku
            int lahutamine = 1 - 1; //lahutamine, kus esimesest arvust lahutatakse maha teine
            double korrutamine = 1 * 2; //korrutamine, kus teine arv korrutatakse esimise arvu kordi.
            double jagamine = 1 / 2; //jagamine. esimine arv jagatakse teise arvuga.
            double astendamine = Math.Pow(2, 2); //astendamine, esimine arv astendatakse teisega
            double juurimine = Math.Sqrt(2); //ruutjuur, parameetrina juuritav arv

            //muutuja nimed 
            int arv = 0;
            string sõne = "abc";
            //string string = "abc"; //kaitsud sõna kasutada ei saa

            // muutuja nimeks ei sobi järgnevad sõnad:
            //abstract, as, base, bool, break, byte, case
            //catch, char, cheched, class, count, continue, decimal,
            //default, delegate, do, double, else, enum, event,
            //explicit, extern, false, finally, fixed, float, for
            //foreach, goto, if, implicit, in, int, interface, internal
            //is, lock, long, namespace, new, null, object, operator,
            //out, override, params, private, protected, public, readonly,
            //ref, return, sbyte, sealed, short, sizeof, stackalloc,
            //static, string, struct, switch, this, throw, try, typeof, uint
            //uint, ulong, unchecked, unsafe, ushort, using, virtual,
            //void, volatile, while.



            //3 kalkulaator ifi ja elsifidega
            Console.WriteLine("Tere. Sisesta esimene arv");
            // Adresserime moodulit "Console", punkti abil ütleme, et kasutame funktsiooni WriteLine 
            // selle jaoks et öelda kasutajale sõnum mis asub funktsiooni nime järel sulgude vahel 
            // ümbritsetuna jutumärkidega. Kasutajale esitatav sõnum on "Tere. Sisesta esimene arv".

            int arv1 = int.Parse(Console.ReadLine());
            //instantsieerime muutuja nimega "arvl", ning selle ette anname andmetüübiks"int", see 
            //ütleb ära, et siin muutujas on täisarvud sees. Omistame muutujale võrdusmärgi abil 
            //väärtuse, mille saame kasutajalt. Selle jaoks, adresseerime uuesti "Console" moodulit 
            //Aga seekord on funktsiooni nimi "ReadLine". Selleks, et käsureapealt tulev arv programmile 
            //tekstina ei näe välja, küsime int mooduli seest omakorda funktsiooni "Parse", ning paneme
            //ReadLine funktsiooni Parse() sulgude vahele.


            Console.WriteLine("Tere. Sisesta teine arv");


            int arv2 = int.Parse(Console.ReadLine());
            Console.WriteLine("Sisesta tehtmärk: / * + -");
            //Adresseerime moodulit "Console" koos "WriteLine" funktsiooniga, et esitada kasutajale 
            //küsimuse "Sisesta tehtemärk: / * + -". Punkti abil saame moodulist Console, funktsiooni 
            //WriteLine, ning sulgude vahel ongi kasutajale esitatav tekst. Tekst ise on ka ümbritsetud
            //jutumärkidega. Lause lõppeb lauselõpumärgiga ";".



            string tehtetyyp = Console.ReadLine();
            //instantsieerime muutuja nimega "tehtetyyp", mille ette kirjutame andmetüübiks "string".
            //Omistame võrdusmärgi abil, sellesse muutujasse kasutajalt sisendi mille saame kasutade.
            //"Console" moodulis oleva ReadLine() funktsiooni abil. Lause lõppeb lauselõpumärgiga ";".


            int tulemus = 0;
            //instantsieerime muutuja nimega "tulemus", andmetüübiga int, ning omistame talle algse 
            //väärtuse võrdusmärgi abil, milleks on 0. Lause lõppeb lauselõpumärgiga ";".


            if (tehtetyyp == "+")
            //teeme tingimuslause if, ning selle tingimuse määrame ära sulgudega,mille vahel on
            //võrdsuskontroll. Kontrollime kas muutuja "tehtetyyp" omab andmeid samalkujul 
            //nagu võrdusmärkidest teisel pool olev tekst "+". Siin lause ei lõppe, kuna tegu ei
            //ole koodiga mis midagi kindlalt veel ära teeb.


            {
                tulemus = arv1 + arv2;
            }
            //peale tingimust on koodiplokk {} sulgude vahel, mis sialdab endas ühte koodirida.
            //selles lauses omistame muutujale "tulemus" võrdusmärgi abil liitmistehte tulemuse,
            //kus liidame kokku muutuja "arv1" ja muutuja "arv2" sisu. Lause lõppeb lauselõpumärgiga ";".


            else if (tehtetyyp == "-")
            //teeme sekundaarse tingimuslause "else if", ning määrame tema tingimuse ära sulgudega.
            //Sulgude vahel on võrdsuskontroll. Kontrollime kas muutuja "tehtetyyp" omab andmeid
            //samal kujul nagu võrdusmärkidest teisel pool olev tekst "-" kui eelnev tingimus ei
            //täitunud. Lause siin ei lõppe, vaid tingimusele järgneb koodiplokk.

            {
                tulemus = arv1 - arv2;
            }
            //peale tingimust on koodiplokk {} loogeliste sulgude vahel, mis sisaldab endas ühte
            //koodirida. selles lauses omistame muutujale "tulemus" võrdusmärgi abil lahutustehte
            //tulemuse, kus lahutame muutuja "arv" sees olevast väärtusest maha "arv2" muutujas
            //oleva väärtuse. Lause lõppeb lauselõpumärgiga ",".

            else if (tehtetyyp == "/")
            //teeme sekundaarse tingimuslause "else if", ning määrassme tema tingimuse ära sulgudega. 
            //Sulgude vahel on võrdsuskontroll. Kontrollime kas muutuja "tehtetyyp" omab andmeid
            //samal kujul nagu võrdusmärkidest teisel pool olev tekst "/" kui eelnev tingimus eʻi
            //täitunud. Lause siin ei lõppe, vaid tingimusele järgneb koodiplokk.
            {
                tulemus = arv1 / arv2;
            }
            //peale tingimust on koodiplokk {} loogeliste sulgude vahel, mis sisaldabendas ühte 
            //koodirida. selles lauses omistame muutujale "tulemus" võrdusmärgi abil korrutustehte 
            //tulemuse, kus korrutame muutujas "arv2" oleva väärtuse, muutujas "arv1" oleva väärtuse
            //kordi. Lause lõppeb lauselõpumärgiga ";".

            else if (tehtetyyp == "*")
            //teeme sekundaarse tingimuslause "else if", ning määrame tema tingimuse ära sulgudega.
            //Sulgude vahel on võrdsuskontroll. Kontrollime kas muutuja "tehtetyyp" omab andmeid
            //samal kujul nagu võrdusmärkidest teisel pool olev tekst "*" kui eelnev tingimus ei
            //täitunud. Lause siin ei lõppe, vaid tingimusele järgneb koodiplokk.
            {
                tulemus = arv1 * arv2;
            }
            //peale tingimust on koodiplokk {} loogeliste sulgude vahel, mis sisaldab endas ühte 
            //koodirida. selles lauses omistame muutujale "tulemus" võrdusmärgi abil korrutustehte 
            //tulemuse, kus korrutame muutujas "arv2" oleva väärtuse muutujas "arv1" oleva väärtuse
            //kordi. Lause lõppeb lauselõpumärgiga ";".

            else if (tehtetyyp == "^")
            //teeme sekundaarse tingimuslause "else if", ning määrame tema tingimuse ära sulgudega.
            //Sulgude vahel on võrdsuskontroll, kontrollime kas muutuja "tehtetyyp" omab andmeid 
            //samal kujul nagu võrdusmärkidest teisel pool olev tekst "^" kui eelnev tingimus ei
            //täitunud. Lause siin ei lõppe, vaid tingimusele järgneb koodiplokk.
            {
                tulemus = (int)Math.Pow(arv1, arv2);
            }
            //peale tingimust on koodiplokk {} loogeliste sulgude vahel, mis sisaldab endas ühte 
            //koodirida. Selles lauses omistatakse võrdusmärgi abil muutujasse "tulemus" mille saame 
            //"Math" moodulist pärineva funktsiooni "Pow()" abil. Math Pow() võtab parameetritena
            //sisse muutjad "arv1" ja "arv2". Esimene parameeter on astendatav, teine parameeter 
            //on astendaja. Funktsiooni Math.Pow() ees on kiirteisendus (int), kuna muutuja 
            //"tulemus" andmetüüp on täisarv. Math Pow() väljund teisendatakse nii täisarvuks.
            //Lause lõppeb lauselöpumärgiga ";".


            else
            //peale kõiki järeltingimusi on meil tingimuslause osa "else" mida täidetakse kõikide 
            //muude tingimuslause osade mittetäitumisel. Siin eraldi tingimust välja ei kirjutada 
            //ning sellest tulenevalt ei ole ka sulge. Järgneb ainult koodiplokk.
            {
                Console.WriteLine("Palun sisesta tehe, mida kalkulaator tavustada oskab");
            }
            //peale "else" on koodiplokk {} loogeliste sulgude vahel, mis sisaldab endas ühte 
            //koodirida. Selles koodireas kasutame moodulist "Console" punkti abil funktsiooni 
            //"WriteLine" et öelda kasutajale "Palun sisesta tehe, mida kalkulaator tuvastada
            //oskab". Koodirida lõppeb lauselõpumärgiga ";".


            Console.WriteLine(tulemus);
            //Kasutame moodulist "Console" punkti abil funktsiooni "WriteLine" et kuvada kasutajale 
            //tehte tulemus. Selle jaoks on WriteLine funktsioonis parameetrina pandud muutuja
            //"tulemus" ilma tekstiks teisendamata. Lause lõppeb lauselõpumärgiga ";".






            //Console.WriteLine("Sisesta ostusumma");
            //double ostusumma = double.Parse(Console.ReadLine());
            //if (ostusumma > 100)
            //{
            //    Console.WriteLine("Saad 20% allahindlust!!!!!!!!!!!!!!!!!!!!!!!!!!!!!");
            //}
            //else if (ostusumma < 101 && ostusumma > 50)
            //{
            //    Console.WriteLine("Saad 10% allahindlust. c: yay");
            //}
            //else if (ostusumma < 51 && ostusumma > 20)
            //{
            //    Console.WriteLine("5% allahindlust.");
            //}
            //else if (ostusumma < 21 && ostusumma > 0)
            //{
            //    Console.WriteLine("allahindlust ei saa");
            //}
            //else
            //{
            //    Console.WriteLine("sisestatud on vigane arv");
            //}





            //string kasutajaNimi = "";
            //do
            //{
            //    Console.WriteLine("Palun sisesta oma kasutajanimi: ");
            //    kasutajaNimi = Console.ReadLine();
            //} while (kasutajaNimi != "user1");
            //if (kasutajaNimi == "user1")
            //{
            //    int ruuduSuurus = 0;

            //    do
            //    {
            //        Console.WriteLine("Kui suurt ruutu saada tahad");
            //        ruuduSuurus = int.Parse(Console.ReadLine());
            //    } while (ruuduSuurus < 0 && ruuduSuurus > 20);

            //    char reaKujund = ' ';
            //    string üksRida = "";
            //    int tsükliMuutuja = ruuduSuurus;

            //    do
            //    {
            //        üksRida = üksRida + ")" + reaKujund;
            //        tsükliMuutuja = tsükliMuutuja - 1;
            //    } while (tsükliMuutuja != 0);

            //    tsükliMuutuja = ruuduSuurus;

            //    do
            //    {
            //        Console.WriteLine(üksRida);
            //        tsükliMuutuja -= 1;
            //    } while (tsükliMuutuja != 0);

            //    Console.WriteLine($"Palun, siin on sinu ruut, suurusega {ruuduSuurus}x{ruuduSuurus}");
            //}

            /* tingimuslause osad */
            if (true) { } //kaitstud sõna "if" kutsub esile tingimuslause, mille tingimus on sulgude vahel, ning millele järgneb
                              //koodiplokk tingimuse täitumisel teostatava koodiga
                else if (true) { } //kaitstud sõnad "else" ja "if" (else if) kutsuvad esile sekundaarse tingimuslause, mille tingimus
                                   //on samamoodi sulgude vahel, ning millele pepab eelnema alat kas "if" või teine "else if". Tingimuse täitumisel
                                   //ja eelneva tingimuse mittetäitumisel, teostatakse koodiploki sees olev kood.
                else { } //kaitstud sõna else kutsub esile järeltingimuse, millele peab eelnema kas "if" või "else if", ning mille koodiploki sisu
                         //täidetakse kõikide teiste "if" ja "else if" tingimuste läbikukkumisel.


            int option = 3; // -------

            switch (option) // "switch" on kaitstud sõna alternatiivse tingimuskontrolli jaoks, mida saab if-else asemel kasutada.
                            // Sulgude vahele käib muutuja nimi, mille põhjal tingimuslik ümberlülitus toimub. 
                            // Siin sulgude vahel ei ole tingimus ise, vaid kõigest kontrollitav muutuja või omakorda sulgude vahel muu tingimus.
                            // Pärast lülitusvalikut tuleb koodiplokk.
            {
                case 1:
                    // Koodiploki sees on erinevad juhtumid, juhtumit sätestatakse kaitstud sõna "case" abil.
                    // Antud juhul kontrollitakse, kas muutuja "option" on väärtus 1, millele järgneb koolon ":".
                    // Väljendades tingimuse täitumisel tehtava kooditegevuse algust.
                    break;
                // Kui tegevus on tehtud, väljutakse mitte ainult juhtumist, vaid kogu käesoleva case-tingimusblokist kaitstud
                //sõnaga "break". Peaele breaki on läuselõpumärk ";".
                //Juhtumeid võib olla mitmeid, antud juhul on neid kolm kindlalt.
                case 2:
                    break;
                case 3:
                    Console.WriteLine(option); //tehtav kooditegevus.
                    break;
                default:    //Default juhtumit täidetakse siis, kui ülejäänud juhtumid ei kirjelda muutujas "option" olevat seisu. 
                    break;  //Ka default lõppeb sõnaga break.
            }

            /* sõne tööriistad ja muud tekstiga seotut */
            string alfa = "a\nb";        // \n -> tekitab ühe sõne sisse reamurde, sõne kus on sees üks "\n", omab kahte rida.
            string beta = $"a {alfa} b"; // $ -> lubab kasutada muutjaid loogeliste sulgudega otse teks sees. On variant
                                         // formateeritud stringist.

            

                /* Tsüklid */
            // 1. do-while
            int dew = 0;
            do // "do" on kaitstud sõna, mis alustab do-while tsüklit. Pärast seda on koodiplokk {} ning ütleb et tee seda koodi
            {
                dew++;
            } while (dew != 5); //niikaua kuni while järel olevate sulgude vahel tingimus ei täitu, käivitatakse eelnev kood uuesti.

            // 2. while
            int i = 1;  //tsüklimuutuja mis aitab järge pidada while tsükli toimimisel
            while (i < 5) // "while" on kaitstud sõna mis alustab while tsükli varianti, ilma "do"-ta, ning vojab alati välist
                          // tsüklimuutuja. antud juhul on selleks i. Tsükli tingimus, mis peale "while" sõna on, asub sulgude vahel,
                          // siin kontrollitaksegi tsükli tööd, läbi kindla tingimuse kasutades tsüklimuutuja.
                          // antud juhul tsükkel töötab niikaua, kuni i on väiksem kui 5. kui i on sama suur nagu 5, siis tsükkel
                          // katkeb.
            {
                // koodiplokk kus midagi tehakse
                i++; // ning seejärel muudetakse tsüklimuutuja "i" olekut. antud juhul liidetakse 1 juurde kiirtehtega "++".
            }
            // 3. for
            int kogus = 6; // muutuja mida tsükkel kasutab oma töö tegemiseks - teisisõnu, töödeldavv materjal
            for (int k = 0; k < kogus; k++) // kaitstud sõnaa "for" alustab for-tsüklit, pärast mida on sulud, mille vahel on kõik tsükli
                                            // töö jaoks vajalik olemas. Esimine parameeter, tekistab tsükli töö jaoks kohaliku muutuja
                                            // "int k =;" mida tsükli ENDA töö juhtimiseks. Teine parameeter on tingimuslause, mis kontrollib
                                            // tingimuse täitumist "k < kogus;" ning mille täitumisel tsükli töö jätkub, aga mille
                                            // mitte - täitumisel tsükkel katkeb. Kolmas parameeter on tsüklimuutuja inkrementeerimine kiirtehtega
                                            // "k++".Pane tähele, et iga sulgude vahel oleva osa järel(välja arvatud viimase) on
                                            // lauselõpumärk.Tsükli tööd kontrolliv tingimuslause koosneb kolmest reast, mitte ühest
                                            // nagu "while" või "do-while" puhul.
                                            // sulgudele järgneb, loogeliste sulgude vahel ole koodiplokk {}
                                            // töötlustegevus tsükli sees, on muutuja "k" hetkearvu väljakuvamine.
            {
                Console.WriteLine(k);
            }
            // 4. foreach
            int[] arvuLoend = { 3, 67, 420, 69, 42 }; //massiiv mida foreach kasutab või töötlebmingil kujul
            foreach (var arvInLoend in arvuLoend) //kaitstud foreach alustab forach tsükli. Pärast mdia on sulud, mille vahel tekitatakse
                                                  //ajutine muutuja andetüübiga "var" töödeldava andmekogumi üksikelemendi jaoks. süntaksis olev
                                                  //kaitstud sõna "in" väljendab et tsükkel käib selle elementide kohta, ming vara "arvInLoend"
                                                  //muutuja hoiab endas just peale sõna "in" olevaandmekogumi elementi. Tsükli ei ole nähtasvat
                                                  //tsüklimuutujat ega tingumust, tsükkel niikaua kuni elemente jätkub, ehk tsükli töö käib
                                                  //iga üksiku elemendi kohta andmekogumis individuaalselt. Tsükli ole vaja tsüklimuutujat, kuna talle on 
                                                  //sisse ehitatatud vaikimisi elemendi järjestuse jälgimine. 
                                                  //peale sulge, on koodiplokk {} kus tehakse mingi tegevus
                                                  //Antud juhul kuvatakse välja ajutine muutuja, mille sees on loendi, hetkel tsüklis olev element.
            {
                Console.WriteLine(arvInLoend);
            }







            /* Loogilised tehted */


            // && -> "and" loogiline tehe, mida kasutatakse tingimuste kirjeldamisel, ning mis annab positiivse vastuse (true) juhul kui
            //       mõlemal pool "&&" märki olevad tingimused on täidetud. Kui üks neist ei ole, siis annab negatiivse vastuse (false).
            // || -> "or"! loogiline tege, mida kasutatakse tingimuste kirjeldamisel, ning mis annab positiivse vastuse (true) siis kui
            //       vähemalt üks tingimus on täidetud. Negatiivne vastus (false) tagastatakse siis, kui kõik tingimused on täitmata.
            // ! -> "not" loogiline tehe, mida kasutatakse tingimuse tulemuse inverteerimiseks. Tulemus, mis muidu tagastaks (true),
            //       hüüumärgi abil tagastab (false), ja vastupidi - tulemus mis muidu tagastaks (false), hüüumärgi abil tagastab (true)

            /* Võrdlusoperaatorid */

            // == --> "on võrdne". Võrdusmärkide ühel pool olev objekt peab vastama täpselt oma olemuselt võrdusmärkide teise pool oleva
            //         objektiga. ei ole sama nagu üks võrdusmärk, üks võrdusmärk omistab, kaks võrdleb.
            // != -> "ei ole võrdne". Võrdusmärgi ühel pool olev objekt *EI TOHI* olla samal kujul nagu võrdusmärgi teisel pool olev objekt.
            //        Ta võib olla ükskõik mis muul kujul, aga mitte võrreldava objektiga samal kujul. Võrdlusoperaator on kombinatsioon
            //        "on võrdne operaatorist, ja loogilisest tehet "not".
            // > -> "on suurem kui". Märgist vasakul pool olev objekt peaks olema suurem, kui paremal pool olev objekt.
            // < -> "on väiksem kui". Märgist vasakul pool olev objekt peaks olema väiksem, kui paremal pool olev objekt.
            // >= -> "suuremvõrdne". Märgist vasakul pool olev objekt peaks olema vähemalt võrdne või suurem kui parempoolne objekt.
            //        Võrdlusoperaator on kombinatsioon "on võrdne" ja "on suurem kui" operaatoritest.
            // <= --> "väiksemvõrdne". Märgist vasakul pool olev objekt peaks olema vähemalt võrdne või väiksem kui parempoolne objekt.
            // Võrdlusoperaator on kombinatsioon "on võrdne" ja "on väiksem kui" operaatoritest.

            /* omistusoperaatorid ja kiirtehted */

            int thing = 1;// =  -> üksik võrdusmärk omistab muutujale sisse väärtuse, mida saab kasutada läbi muutuja nime.
                thing += 1;   // += -> võrdusmärk mille ees on pluss, automaatselt liidab muutujale otsa võrdusmärgi teisel pool oleva arvu.
                              //       asendab tehet "thing = thing + 1". on kombinatsioon matemaatilisest tehetest "+" ja omistamisest "=".
                thing -= 1;   // -= -> võrdusmärk mille ees on miinus, automaatselt lahutab muutujast maha võrdusmärgi teisel pool oleva arvu.
                              // asendab tehet "thing = thing - 1". on kombinatsioon matemaatilistest tehetest "-" ja omistamisest "=".

                thing *= 2;  // *= -> võrdusmärk mille ees on korrutusmärk "*", automaatselt korrutab muutuja sisu, võrdusmärgi teisel pool oleva arvu kordi.
                             // asendab tehet "thing = thing * 2". on kombinatsioon matemaatilistest tehetest "*" ja
                             // omistamisest "=".
                thing /= 2;  // /= -> võrdusmärk mille ees on jagamismärk "/", automaatselt jagab muutuja sisu võrdusmärgi teisel pool oleva
                             // arvu osadeks. asendab tehtet "thing = thing / 2". on kombinatsioon matemaatilisest tehtest "/" ja
                             // omistamisest "=".

                thing++;      // ++ -> on spetsifiiliselt ühe juurde liitmiseks kiirtehe.
                thing--;      // -- -> on spetsifiiliselt ühe maha lahutamiseks kiirtehe.

                /* Tsüklid */
                // 1. do-while
                do // "do" on kaitstud sõna, mis alustab do-while tsüklit. Pärst seda on koodiplokk {} ning ütleb et tee seda koodi 
                {

                } while (true); //niikaua kuni while järel olevate sulgude vahel tingimus ei täitu, käivitatakse eelnev kood uuesti.

            }
        }
    }

