package bid.itbox.util;

import static org.junit.Assert.assertEquals;

import java.util.Arrays;
import java.util.Collection;

import org.junit.After;
import org.junit.AfterClass;
import org.junit.Before;
import org.junit.BeforeClass;
import org.junit.Ignore;
import org.junit.Test;
import org.junit.runner.RunWith;
import org.junit.runners.Parameterized;
import org.junit.runners.Parameterized.Parameters;

/*
 * 注解
 * @setUpBeforeClass:是在所以的方法执行之前执行，
 * 可用来加载配载文件等
 * @tearDownAfterClass:在有所的方法执行之后执行，可用用来释放资源等
 * @setUp:在每个方法执行前都会执行
 * @tearDown:在每个方法执行后都会执行
 * @Test:将普通方法修饰为测试方法
 * @Test(expected=XX.class)
 * @Test(expected=XX.class)
 * @Ignore:忽略测试
 * @RunWith:可以更改测试运行器org.junit.runner.Runner
 * @Parameters:配置测试参数
 */
@RunWith(Parameterized.class)
public class JunitFlow {
	int expected=0;
	int param1=0;
	int param2=0;
	@BeforeClass
	public static void setUpBeforeClass() throws Exception {
		System.out.println("setUpBeforeClass");
	}

	@AfterClass
	public static void tearDownAfterClass() throws Exception {
		System.out.println("tearDownAfterClass");
	}

	@Before
	public void setUp() throws Exception {
		System.out.println("setUp");
	}

	@After
	public void tearDown() throws Exception {
		System.out.println("tearDown");
	}

	@Test
	public void test1() {
		System.out.println("test1");
	}

	@Test
	public void test2() {
		System.out.println("test3");
	}
	@Test
	public void testAdd(){
		assertEquals(9, new Calculate().add(1,8));
	}
	@Test
	public void testSubtract(){
		assertEquals(1, new Calculate().subtract(10, 11));
	}
	@Test
	public void testMultiply(){
		assertEquals(100, new Calculate().multiply(10, 10));
	}
	@Test
	public void testDivision(){
		assertEquals(10, new Calculate().division(10, 100));
	}
	@Test(expected=ArithmeticException.class)
	public void testDivisionException(){
		assertEquals(10, new Calculate().division(0, 100));
	}
	@Ignore("这只是一个示例而已不测试")
	@Test(timeout=30)
	public void testWhile(){
		while (true) {
			System.out.println("While...........");
		}
	}
	
	@Parameters
	public static Collection<Object[]> t(){
		return Arrays.asList(new Object[][]{
			{3,2,1},
			{6,3,3}
		});
	}
	
	public JunitFlow(int expected,int param1,int param2) {
		// TODO Auto-generated constructor stub
		this.param1=param1;
		this.param2=param2;
		this.expected=expected;
	}
	@Test
	public void testAdd2(){
		assertEquals(expected, new Calculate().add(param1, param2));
	}
}
