# Docker Sift

Mikäli VMWare / VBOx ei toimi jostain syystä SIFT.ova:n kanssa, voit käyttää dockeria.

## Ohjeet

1. Lataa ja asenna Docker: https://www.docker.com/products/docker-desktop/

2. Lataa Dockerfile tältä sivulta (tai kloonaa tämä repo)

3. Aja samassa hakemistossa jossa sinulla on tämä Dockerfile terminaalista:
docker built -t sift .

4. Docker raksuttaa hetken, jonka jälkeen voit käynnistää kontin: 
docker run -d -v (polku jossa kurssin data on):/cases -p 2022:22 sift

esim.
docker run -d -v /home/juho/kurssi/:/cases -p 2022:22 sift

5. Sen jälkeen voit yhdistää sift koneelle seuraavasti:
ssh sansforensics@localhost -p 2022

Salasana: forensics