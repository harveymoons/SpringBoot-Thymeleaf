###### RESTFul
```java
@GetMapping // get 
@PostMapping // post
@PutMapping // update[All]
@DeleteMapping // delete
```
  
###### @RequestBody / @ResponseBody
```java
@RequestBody // 요청을 http body 에 받아 올 때
@ResponseBody // 응답을 http body 에 담아 보낼 때 / return 값이 없어도 적용하는 것이 좋다
```
[Ref.] https://kimdonghyungsoo.tistory.com/8  


###### @Controller / @RestController
```java
@Controller // return을 view로 한다 data를 포함할 수 있다 
@RestController // data만 return 한다
```
  
###### @PostMapping + return Type String
호출한 결과를 다른 뷰로 넘길 때 사용하는 조합
```java
@PostMapping("/findAllTestDev")
public String findAllTestDev(TestDevVo vo, Model model) throws Exception{
		
		model.addAttribute("testData", testService.findAllTestDev(vo));
		return "test/tableContents";
}
```
  
###### @PostMapping + @ResponseBody
요청한 곳으로 응답을 반환할 때 사용하는 조합  
`post메서드`는 `body`에 `요청`할 내용을 담아서 전달하고 `응답`받을 내용도 `body`로 받는다
```java
@PostMapping("/registerTestDev")
@ResponseBody public Long registerTestDev(TestDevVo vo) throws Exception{
		
		return testService.registerTestDev(vo);
}
```
  
###### @NotBlank / @NotNull / @NotEmpty / @range / @length
  
  
###### @Transactional
- public 메소드에만 선언한다
  
###### @ModelAttribute
- 요청 파라미터를 앞에 선언해준다 
- 주의할 것은 파라미터 필드중 null 값이 있으면 에러가 발생한다  
  
###### Use Cache
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-cache</artifactId>
</dependency>
```
```java
@EnableCaching
@SpringBootApplication
public class MyApplication {
    public static void main(String[] args) {
        SpringApplication.run(MyApplication.class, args);
    }
}

@Service
public class TestService {
    private List<String> list;
    
    @PostConstruct
    public void init() {
        list = new ArrayList<>();
    }
    
    @Cacheable(value="test")
    public String getInformation(String info) {
        try {
            Thread.sleep(3000);
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
        return list.stream().filter(x->x.equals(info)).findFirst().get();
    }
    
    @CacheEvict(value="test")
    public void createInformation(String info) {
        list.add(info);
    }
}
```
[Ref.] https://jeong-pro.tistory.com/170  
  
  
