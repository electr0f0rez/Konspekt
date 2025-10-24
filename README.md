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

            string kasutajaNimi = "";
            do
            {
                Console.WriteLine("Palun sisesta oma kasutajanimi: ");
                kasutajaNimi = Console.ReadLine();
            } while (kasutajaNimi != "user1");
            if (kasutajaNimi == "user1")
            {
                int ruuduSuurus = 0;

                do
                {
                    Console.WriteLine("Kui suurt ruutu saada tahad");
                    ruuduSuurus = int.Parse(Console.ReadLine());
                } while (ruuduSuurus < 0 && ruuduSuurus > 20);

                char reaKujund = ' ';
                string üksRida = "";
                int tsükliMuutuja = ruuduSuurus;

                do
                {
                    üksRida = üksRida + ")" + reaKujund;
                    tsükliMuutuja = tsükliMuutuja - 1;
                } while (tsükliMuutuja != 0);

                tsükliMuutuja = ruuduSuurus;

                do
                {
                    Console.WriteLine(üksRida);
                    tsükliMuutuja -= 1;
                } while (tsükliMuutuja != 0);

                Console.WriteLine($"Palun, siin on sinu ruut, suurusega {ruuduSuurus}x{ruuduSuurus}");
                //}

                /* tingimuslause osad */
                if (true) { } //kaitstud sõna "if" kutsub esile tingimuslause, mille tingimus on sulgude vahel, ning millele järgneb
                              //koodiplokk tingimuse täitumisel teostatava koodiga
                else if (true) { } //kaitstud sõnad "else" ja "if" (else if) kutsuvad esile sekundaarse tingimuslause, mille tingimus
                                   //on samamoodi sulgude vahel, ning millele pepab eelnema alat kas "if" või teine "else if". Tingimuse täitumisel
                                   //ja eelneva tingimuse mittetäitumisel, teostatakse koodiploki sees olev kood.
                else { } //kaitstud sõna else kutsub esile järeltingimuse, millele peab eelnema kas "if" või "else if", ning mille koodiploki sisu
                         //täidetakse kõikide teiste "if" ja "else if" tingimuste läbikukkumisel.

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
}
