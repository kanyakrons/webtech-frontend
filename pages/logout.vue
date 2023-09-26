<script setup lang="ts">
  import { useAuthStore } from '~/stores/useAuthStore';
  const auth = useAuthStore()
  
  const { data: response, error } = await useMyFetch<any>('auth/me', {
      method: 'POST',
    })
  if(response.value !== null){
    auth.clear()
  }
  </script>