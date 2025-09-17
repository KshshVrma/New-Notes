---
doc_type: hypothesis-highlights
url: 'https://chatgpt.com/c/679e3735-8928-800e-aa0d-cfe9fe13d7f9'
---
[[Toggles]]
# ChatGPT

## Metadata
- Author: [chatgpt.com]()
- Title: ChatGPT
- Reference: https://chatgpt.com/c/679e3735-8928-800e-aa0d-cfe9fe13d7f9
- Category: #article

## Page Notes
## Highlights

- What is Togglz in Spring Boot?
- Togglz is a feature toggle (or feature flag) library for Java applications, including Spring Boot. It allows developers to enable or disable features dynamically without deploying new code. This is useful for:Gradual rollouts (enabling a feature for a small group before full release).A/B testing (showing different features to different users).Canary releases (testing features in production for a subset of users).Rolling back features easily in case of issues. 


Add Dependency

Define Feature Flags
import org.togglz.core.Feature;
import org.togglz.core.annotation.Label;
import org.togglz.core.context.FeatureContext;

public enum MyFeatures implements Feature {
    
    @Label("New Payment Flow")
    NEW_PAYMENT_FLOW,
    
    @Label("Dark Mode")
    DARK_MODE;

    public boolean isActive() {
        return FeatureContext.getFeatureManager().isActive(this);
    }
}

#### **Configure Togglz**

Create a feature manager bean:

@Configuration
public class TogglzConfig {

    @Bean
    public FeatureManager featureManager() {
        return new FeatureManagerBuilder()
            .featureEnum(MyFeatures.class)
            .stateRepository(new FileBasedStateRepository(new File("/tmp/features.properties")))
            .build();
    }
}

#### **Use Togglz in Code**

You can check feature status in your application logic:

if (MyFeatures.NEW_PAYMENT_FLOW.isActive()) {
    System.out.println("New payment flow enabled");
} else {
    System.out.println("Using old payment system");
}

#### **Enable UI to Manage Features**

Togglz provides a web UI for toggling features dynamically. Enable it in `application.properties`:
togglz.console.enabled=true
togglz.console.path=/togglz


Now, access `http://localhost:8080/togglz` to toggle features.


### **Advanced Usage**

1. **Enable Features for Specific Users**  
    You can configure Togglz to enable features for admin users or a percentage of users:

public class CustomUserProvider implements UserProvider {
    @Override
    public FeatureUser getCurrentUser() {
        return new SimpleFeatureUser("admin", true);
    }
}
