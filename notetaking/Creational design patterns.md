[[lld roadmap]]

singleton dp: private constructor, getInstance method, (generally hava a single instance)

class Singleton {
    private static Singleton instance;

    private Singleton() { } // Private constructor

    public static Singleton getInstance() {
        if (instance == null) {
            instance = new Singleton(); // Lazily initialized
        }
        return instance;
    }
}