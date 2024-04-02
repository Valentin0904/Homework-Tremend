# Utilizează o imagine Java cu kit de dezvoltare (JDK) ca bază
FROM openjdk:11

# Setează directorul de lucru în container
WORKDIR /app

# Copiază fișierul sursă Java în container
COPY Main.java /app

# Compilează aplicația Java
RUN javac Main.java

# Comandă pentru a rula aplicația
CMD ["java", "Main"]
