Zadanie 1 
Napisz funkcję election_statistics, która będzie tworzyła obiekt typy Data Frame z jedną z następujących
statystyk:
• Frekwencja ogółem (liczba kart wyjętych z urn/ liczba osób uprawnionych do głosowania) (‘frekwencja’)
• Udział głosów nieważnych (chodzi o nieważne głosy, a nie karty) w całkowitej liczbie oddanych głosów (‘głosy nieważne’)
• Udział wyborców głosujących na podstawie zaświadczenia o prawie do głosowania w całkowitej liczbie oddanych głosów (‘zaświadczenia’)
Funkcja election_statistics powinna przyjmować następujące argumenty:
• year = lista, domyślnie [2015, 2019, 2023]
• jst – string określający czy funkcja ma przedstawiać statystyki na poziomie gminy, powiatu czy
województwa (tj, ‘gmina’, ‘powiat’, ‘województwo’), domyślnie funkcja powinna generować
statystyki na poziomie powiatu,
• jst_number – domyślna wartość 10,
• sort – domyślna wartość logiczna True dla sortowania od wartości najmniejszej do największej
(False dla sortowania od wartości największej do najmniejszej),
• sort_year = numer indeksu z listy year,
• stat = ‘frekwencja’, ‘głosy nieważne’, ‘zaświadczenia’

Przykład zastosowania:
election_statistics(year = [2015, 2019], jst=’powiat’, jst_number=8, sort=True, stat=‘frekwencja’)
Powyższa funkcja powinna zwrócić ramkę danych z nazwami 8 powiatów (dodatkowo także w osobnej kolumnie nazwę województwa, w którym się znajdują), w których w 2019 roku (ostatni element z listy ‘year’) odnotowano najniższą frekwencję w wyborach do Sejmu łącznie z poziomem tej frekwencji w tych powiatach w 2015 i 2019 roku.
election_statistics(year = [2015, 2023], jst=’gmina’, jst_number=8, sort=False, stat=‘zaświadczenia’)
Powyższa funkcja powinna zwrócić ramkę danych z nazwami 8 gmin (dodatkowo także w osobnych kolumnach nazwy powiatu i województwa), w których w 2023 roku (ostatni element z listy ‘year’) odnotowano najwyższy udział osób głosujących na podstawie zaświadczeń o prawie do głosowania w wyborach do Sejmu łącznie z wysokością tych udziałów w tych gminach w 2015 i 2023 roku.



Zadanie 2 
Napisz funkcję election, która będzie tworzyła obiekt Data Frame porównujący przeciętne wartości poniższych statystyk we wskazanych latach wyborczych dla n powiatów uszeregowanych według łącznej liczby oddanych głosów (malejąco):
• procentowe poparcie dla poszczególnych obozów politycznych (poparcie liczymy jako procentowy udział oddanych głosów na dany obóz polityczny),
• stopa bezrobocia rejestrowanego
• przeciętne wynagrodzenie brutto (przyjmij, że wynagrodzenie w 2023 roku jest takie samo,
jakie było w 2022 roku).

Funkcja election_data powinna przyjmować następujące argumenty:
• year = lista, domyślnie [2015, 2019, 2023]
• parties = lista stringów z nazwami obozów politycznych,
• count – liczba określająca liczbę powiatów uwzględnionych w analizie, domyślnie 1,
