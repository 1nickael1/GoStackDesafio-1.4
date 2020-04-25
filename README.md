*Desafio 04: Conceitos do React Native*

Para corrigir o erro de Network, basta adicionar o trecho a seguir em 
> /android/app/src/main/AndroidManifest.xml

<manifest ...>
    <uses-permission android:name="android.permission.INTERNET" />
    <application
        ...
        android:usesCleartextTraffic="true"  // <-- Verifique se essa linha esta contida no application
        ...>
        ...
    </application>
</manifest>

Se o error persistir, troque a baseURL do axios de localhost para seu IP adicionando http://