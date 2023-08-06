# Notes-Password-Manager
/* Embrace the power of organization with our online Android app! Seamlessly take notes anytime and generate robust password for heightened account security. It’s like having two aps in one, always at your service whenever you need them. Simplify your life and keep everything in one place with ease! */
dependencies {
// Import from the Firebase platform
implementation
platform('com.google.firebase:firebase-bom:26.3.0')
// Declare the dependency for the Firebase Authentication library
// When using the BoM, you don't specify versions in Firebase
library dependencies{
implementation 'com.google.firebase:firebase-auth'
}
public static String generateRandomPassword(int len) {
String chars = "0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghi"
+"jklmnopqrstuvwxyz!@#$%&";
Random rnd = new Random();
StringBuilder sb = new StringBuilder(len);
for (int i = 0; i < len; i++)
sb.append(chars.charAt(rnd.nextInt(chars.length())));
return sb.toString();
}
