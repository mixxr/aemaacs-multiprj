
package com.adobe.training.core.servlets;

import java.io.IOException;

import javax.servlet.ServletException;
import javax.servlet.http.HttpServletResponse;

import org.junit.jupiter.api.Test;
import org.junit.jupiter.api.extension.ExtendWith;

import io.wcm.testing.mock.aem.junit5.AemContext;
import io.wcm.testing.mock.aem.junit5.AemContextExtension;
import org.mockito.Mockito;

import static org.junit.jupiter.api.Assertions.assertEquals;

import org.apache.sling.api.resource.Resource;

import com.adobe.cq.dam.cfm.ContentFragment;
import com.adobe.cq.dam.cfm.FragmentTemplate;
import com.day.cq.wcm.api.*;
import org.junit.jupiter.api.BeforeEach;

import io.wcm.testing.mock.aem.dam.*;

@ExtendWith(AemContextExtension.class)
class CFModelTest {

    private AemContext context = new AemContext();

    //private com.adobe.training.core.servlets.TagServlet tagServlet;

    @BeforeEach
	void setUp() throws Exception {
		//tagServlet = context.registerService(new TagServlet()); // com.adobe.training.core.servlets.TagServlet;
        System.out.println("CFModelTest.setUp()");
        registerInjectActivateService(new MockAemDamAdapterFactory());

        context.load().json("/cfmodels.json", "/conf/wknd");
        //context.load().json("/cf.json", "/content/dam/wknd/en/adventures/bali-surf-camp/bali-surf-camp");
        
        //context.load().json("/testtags-page.json", "/content/sample/en");
    }

    @Test
    void getCFModel(AemContext context) throws ServletException, IOException, WCMException {
        Resource resource = context.resourceResolver().getResource("/conf/wknd/settings/dam/cfm/models/adventure");
        //Resource cfResource = context.resourceResolver().getResource("/content/dam/wknd/en/adventures/bali-surf-camp/bali-surf-camp");
        FragmentTemplate cfTemplate = resource.adaptTo(FragmentTemplate.class);
        
        //ContentFragment cf = cfResource.adaptTo(ContentFragment.class);
        FragmentTemplate fragmentTemplate = Mockito.mock(FragmentTemplate.class);
        

        //assertEquals(HttpServletResponse.SC_OK, context.response().getStatus());

        System.out.println("####### cfTemplate="+cfTemplate+",resource.version="+resource.getValueMap().containsKey("version"));
        //System.out.println("#### cf="+cf.getTitle());
        //System.out.println("#### cf.template="+cf.getTemplate());

        //System.out.println("#### cfTemplate.getPath()()="+cfTemplate.getTitle());
    }
}
