<script>
	import '../app.postcss';
	let newTodo = 'Eat';

	/**
	 * @type {any[]}
	 */
	let arr = [];

	const handleTodo = () => {
		const todo = arr.push(newTodo);
		console.log(todo)
	};
</script>

<div class="flex justify-center text-2xl font-bold mt-4">SvelteTodo</div>

<div class="mb-4 w-96 mx-auto mt-32 flex">
	<input
		class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
		id="username"
		type="text"
		placeholder="Todo..."
		on:change={() => {
			newTodo = 'Eat';
		}}
	/>
	<div class="flex space-x-2 justify-center ml-4">
		<button
			on:click={() => handleTodo()}
			type="button"
			class="inline-block px-6 py-2.5 bg-blue-600 text-white font-medium text-xs leading-tight uppercase rounded shadow-md hover:bg-blue-700 hover:shadow-lg focus:bg-blue-700 focus:shadow-lg focus:outline-none focus:ring-0 active:bg-blue-800 active:shadow-lg transition duration-150 ease-in-out"
			>Add Todo</button
		>
	</div>
</div>
<div>
	<div class="text-2xl mt-20 flex justify-center font-bold">Todos for Today</div>
</div>

<slot />
