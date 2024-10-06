* 
    ```
    @Bean
    @ConditionalOnMissingBean
    public Decoder feignDecoder(ObjectProvider<HttpMessageConverterCustomizer> customizers) {
        return new OptionalDecoder(new ResponseEntityDecoder(new SpringDecoder(messageConverters, customizers)));
    }
    ```
  * if NO other "feign.codec.Decoder" is created -> `OptionalDecoder` is created
* TODO: