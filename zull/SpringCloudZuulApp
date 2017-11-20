package zuul.zuul.main;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.cloud.netflix.zuul.EnableZuulProxy;
import org.springframework.context.annotation.Bean;
import org.springframework.core.io.ClassPathResource;

import zuul.zuul.filter.ErrorFilter;
import zuul.zuul.filter.PostFilter;
import zuul.zuul.filter.PreFilter;
import zuul.zuul.filter.RouteFilter;

@SpringBootApplication
@EnableZuulProxy
public class SpringCloudZuulApp 
{
    public static void main( String[] args )
    {
//    	 Object[] sources = {SpringCloudZuulApp.class, new ClassPathResource("application.yml")};
    	SpringApplication.run( SpringCloudZuulApp.class, args );
    }
    
	@Bean
	public PreFilter preFilter() {
		return new PreFilter();
	}

	@Bean
	public PostFilter postFilter() {
		return new PostFilter();
	}

	@Bean
	public ErrorFilter errorFilter() {
		return new ErrorFilter();
	}

	@Bean
	public RouteFilter routeFilter() {
		return new RouteFilter();
	}    
}
